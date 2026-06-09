# 🌤️ Weather Dashboard

A modern, responsive weather dashboard that fetches real-time weather data from the OpenWeatherMap API. Get current weather conditions, 5-day forecasts, and hourly weather updates for any city in the world.

## ✨ Features

- **Current Weather Display**: Real-time temperature, conditions, humidity, wind speed, pressure, and visibility
- **5-Day Forecast**: Visual forecast cards showing min/max temperatures and weather conditions
- **Hourly Forecast**: Detailed hourly weather predictions (up to 12 hours)
- **City Search**: Search for weather information by city name
- **Geolocation**: Automatically fetch weather for your current location
- **Recent Searches**: Quick access to previously searched cities (stored in localStorage)
- **Responsive Design**: Fully responsive and mobile-friendly interface
- **Beautiful UI**: Modern gradient backgrounds, smooth animations, and intuitive layout

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection
- OpenWeatherMap API key (free tier available)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/dmardonesv/himno.git
cd himno
```

2. Get a free API key:
   - Visit [OpenWeatherMap](https://openweathermap.org/api)
   - Sign up for a free account
   - Generate an API key
   - Replace `f4c7cca0d5a2df8901e00f72c9e0d8d2` in `script.js` with your API key

3. Open `index.html` in your browser

### Usage

**Search by City:**
1. Enter a city name in the search box
2. Click "Search" or press Enter
3. View the current weather and forecasts

**Use Current Location:**
1. Click the "📍 Use My Location" button
2. Allow browser permissions for geolocation
3. Weather data for your location will load automatically

**Quick Access:**
- Click any city in the "Recent Searches" section to quickly view its weather again

## 📁 Project Structure

```
himno/
├── index.html          # HTML structure
├── styles.css          # CSS styling and animations
├── script.js           # JavaScript functionality
└── README.md           # Documentation
```

## 🎨 Customization

### API Key

Update the `API_KEY` variable in `script.js`:
```javascript
const API_KEY = 'your_api_key_here';
```

### Units

Change temperature units (Celsius/Fahrenheit) by modifying the `units` parameter in API calls:
```javascript
// For Fahrenheit
units=imperial

// For Celsius (default)
units=metric
```

### Color Scheme

Modify CSS variables in `styles.css`:
```css
:root {
    --primary-color: #2c3e50;
    --secondary-color: #3498db;
    --accent-color: #e74c3c;
    /* ... more variables */
}
```

## 🔌 API Integration

This project uses the **OpenWeatherMap API** with the following endpoints:

### Endpoints Used

1. **Geocoding API**: Convert city names to coordinates
   ```
   https://api.openweathermap.org/geo/1.0/direct?q={city}&limit=1&appid={API_KEY}
   ```

2. **Current Weather API**: Get current weather data
   ```
   https://api.openweathermap.org/data/2.5/weather?lat={lat}&lon={lon}&units=metric&appid={API_KEY}
   ```

3. **Forecast API**: Get 5-day, 3-hour forecast
   ```
   https://api.openweathermap.org/data/2.5/forecast?lat={lat}&lon={lon}&units=metric&appid={API_KEY}
   ```

## 📊 Data Displayed

### Current Weather
- Temperature and "feels like" temperature
- Weather condition (Clear, Rainy, Cloudy, etc.)
- Humidity percentage
- Wind speed
- Atmospheric pressure
- Visibility distance

### Forecast
- 5-day forecast with min/max temperatures
- Weather condition icons
- Hourly breakdown for next 12 hours

## 🌐 Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## ⚠️ Important Notes

### Free Tier Limitations

The free tier of OpenWeatherMap API has some limitations:
- Limited API calls per minute (60/minute)
- Limited API calls per month (1,000,000/month)
- Updates every 10 minutes

### CORS

If you encounter CORS issues when deploying:
1. Use a backend proxy to forward requests
2. Consider using a CORS proxy service
3. Set up your own backend API

### Geolocation

Geolocation requires:
- HTTPS protocol (or localhost for development)
- User permission to access location data

## 🛠️ Development

### Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Grid, Flexbox, Gradients, Animations
- **Vanilla JavaScript**: No dependencies
- **Fetch API**: For HTTP requests
- **LocalStorage API**: For storing recent searches
- **Geolocation API**: For location-based weather

### Browser DevTools Tips

- Use Network tab to monitor API calls
- Check Console for any JavaScript errors
- Use Device Emulation for responsive testing

## 🐛 Troubleshooting

### Weather data not loading?

1. **Check API Key**: Verify your OpenWeatherMap API key is correct
2. **Network Connection**: Ensure you have internet access
3. **CORS Issues**: Check if requests are being blocked by CORS
4. **API Rate Limit**: Wait a few moments if you've made many requests quickly

### Geolocation not working?

1. **HTTPS Required**: Use HTTPS or localhost
2. **Permissions**: Check browser geolocation permissions
3. **Browser Support**: Ensure your browser supports Geolocation API

### Data shows "City not found"?

1. **Spelling**: Double-check city name spelling
2. **Country Code**: Try adding country code (e.g., "London, GB")
3. **City Availability**: Some very small towns may not be in the database

## 📦 Performance

- Lightweight with no external dependencies
- Optimized CSS animations using GPU acceleration
- Efficient API call management
- LocalStorage for instant recent searches

## 🔐 Security

- API key should be protected in production
- Consider using a backend proxy for API calls
- Sensitive data is not stored locally

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📞 Support

For issues or questions:
1. Check the troubleshooting section
2. Visit [OpenWeatherMap Documentation](https://openweathermap.org/api)
3. Create an issue in the repository

## 🎯 Future Enhancements

- [ ] Multi-language support
- [ ] Weather alerts and notifications
- [ ] Historical weather data
- [ ] Multiple location comparison
- [ ] Weather charts and graphs
- [ ] Air quality index
- [ ] UV index
- [ ] Sunrise/Sunset times
- [ ] Dark mode toggle
- [ ] PWA support for offline functionality

---

Made with ❤️ by [dmardonesv](https://github.com/dmardonesv)
