# 🌍 Antipode Explorer

An interactive web application to discover antipodal points — locations on Earth directly opposite to each other through the planet's core.

![Antipode Explorer](https://img.shields.io/badge/version-1.0.0-blue) ![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

### Core Functionality
- **🌐 3D Globe View** — Interactive globe with atmosphere effects and smooth rotation
- **🗺️ 2D Map View** — Traditional flat Mercator projection toggle
- **📍 Click to Find Antipode** — Click anywhere to instantly see the opposite point on Earth
- **🔍 Coordinate Search** — Jump to specific latitude/longitude coordinates

### Visual Enhancements
- **🏳️ Country Flags** — Displays flag emojis for both locations (or 🌊 for ocean)
- **✨ Animated Arc** — Pulsing great-circle arc connecting antipodal points
- **🎨 Premium Dark Theme** — Modern glassmorphism UI with gradient accents

### Advanced Features
- **📱 Split-Screen Mode** — Side-by-side view of both locations simultaneously
- **📸 Export Screenshot** — Save the current view as a PNG image
- **📜 History Panel** — Track previously explored antipode pairs (persisted in localStorage)
- **🔄 Auto-Rotate** — Optional globe auto-rotation for visual effect
- **✈️ Fly-To Animations** — Smooth camera transitions to either location

## 🚀 Quick Start

### Option 1: Direct File Open
Simply open `index.html` in a modern web browser.

### Option 2: Local Server (Recommended)
```bash
# Navigate to the project directory
cd antipode

# Start a local server
python3 -m http.server 8080

# Open in browser
open http://localhost:8080
```

## 🎮 How to Use

1. **Select a Location** — Click anywhere on the globe or map
2. **View Antipode** — See the opposite point with coordinates and location names
3. **Toggle Views** — Switch between 3D Globe and 2D Map modes
4. **Enable Split View** — Click "Split View" to see both points simultaneously
5. **Search Coordinates** — Enter lat, lng (e.g., `40.7128, -74.0060`) to jump to a location
6. **Export** — Click "Export" to download a screenshot
7. **History** — Click any history item to revisit a previous exploration

## 🛠️ Technologies

| Technology | Purpose |
|------------|---------|
| [MapLibre GL JS](https://maplibre.org/) | Interactive map rendering with globe projection |
| [CARTO Basemaps](https://carto.com/) | Dark-themed map tiles |
| [Nominatim](https://nominatim.org/) | Reverse geocoding for location names |
| [html2canvas](https://html2canvas.hertzen.com/) | Screenshot export functionality |
| Vanilla CSS | Glassmorphism UI with CSS variables |

## 📐 How Antipodes Work

An antipode is the point on Earth's surface diametrically opposite to any given point. The calculation is simple:

```javascript
function getAntipode(lng, lat) {
    const newLat = -lat;
    const newLng = lng > 0 ? lng - 180 : lng + 180;
    return [newLng, newLat];
}
```

**Fun fact:** Only ~4% of Earth's land has land antipodes. Most land points have their antipode in the ocean!

## 🌏 Notable Antipode Pairs

| Location A | Location B |
|------------|------------|
| Madrid, Spain | Wellington, New Zealand |
| Hawaii, USA | Botswana, Africa |
| Beijing, China | Argentina |
| Bermuda | Perth, Australia |

## 📁 Project Structure

```
antipode/
├── index.html      # Complete single-file application
└── README.md       # This file
```

## 🌐 Browser Compatibility

- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 14+
- ✅ Edge 80+
