# 🌧️ Rainfall Analysis with Interactive Map

An interactive Jupyter notebook that visualizes rainfall data across India with time-series mapping and rain emoji indicators.

## 📋 Project Overview

This project analyzes historical rainfall data across Indian subdivisions from 1901 to 2017, presenting the data through an interactive map with time slider functionality. The visualization uses intuitive rain emojis to represent different rainfall intensities, making it easy to understand precipitation patterns across time and geography.

## ✨ Features

### 🗺️ Interactive Map
- **Time Slider**: Navigate through years from 1901 to 2017
- **Play Button**: Automatically animate through years to observe rainfall trends
- **Rain Emojis**: Visual representation of rainfall intensity:
  - 🌤️ Light rain (< 100mm)
  - 🌦️ Light to moderate rain (100-500mm)
  - 🌧️ Moderate rain (500-1000mm)
  - ⛈️ Heavy rain (1000-2000mm)
  - 🌊 Very heavy rain (> 2000mm)

### 📊 Data Visualization
- **Circle markers** sized proportionally to rainfall amount
- **Color-coded indicators** with blue intensity representing rainfall levels
- **Interactive tooltips** for quick information on hover
- **Detailed popups** with comprehensive rainfall data on click
- **Seasonal analysis** functionality for specific time periods

### 🎯 Interactive Elements
- Hover tooltips showing location and rainfall amount
- Click popups with detailed subdivision information
- Responsive circle sizing based on precipitation levels
- Smooth time-based animation capabilities

## 🚀 Installation

### Prerequisites
- Python 3.7+
- Jupyter Notebook or JupyterLab

### Required Packages
```bash
pip install pandas numpy matplotlib seaborn folium ipywidgets
```

Or install from the notebook:
```python
!pip install folium ipywidgets
```

## 📂 Data

The project uses `Rainfall_Data_LL.csv` which contains:
- **Time Range**: 1901-2017 (117 years)
- **Geographic Coverage**: Indian subdivisions with latitude/longitude coordinates
- **Measurements**: Monthly and seasonal rainfall data (mm)
- **Subdivisions**: Multiple regions across India

### Data Columns
- `SUBDIVISION`: Geographic region name
- `YEAR`: Year of measurement
- `JAN` to `DEC`: Monthly rainfall data
- `ANNUAL`: Total annual rainfall
- `Jan-Feb`, `Mar-May`, `June-September`, `Oct-Dec`: Seasonal aggregates
- `Latitude`, `Longitude`: Geographic coordinates

## 🎮 Usage

### Basic Usage
1. Clone the repository
2. Install required packages
3. Open `rainfall_analysis.ipynb` in Jupyter
4. Run all cells sequentially
5. Interact with the time slider and play button

### Creating Maps
```python
# Create map for specific year
map_2010 = create_rainfall_map(2010)
display(map_2010)

# Create seasonal analysis
monsoon_map = create_seasonal_rainfall_map(2010, 'June-September')
display(monsoon_map)
```

### Interactive Widget
```python
# Display interactive widget with time slider
interactive_widget = interactive_rainfall_map()
display(interactive_widget)
```

## 🔧 Functions

### Core Functions
- `create_rainfall_map(year)`: Creates map for specific year
- `create_seasonal_rainfall_map(year, season)`: Creates seasonal rainfall map
- `interactive_rainfall_map()`: Creates interactive widget with time slider
- `get_rain_emoji(rainfall)`: Returns appropriate emoji for rainfall amount
- `get_rain_color(rainfall)`: Returns color based on rainfall intensity

### Available Seasons
- `'Jan-Feb'`: Winter season
- `'Mar-May'`: Pre-monsoon season
- `'June-September'`: Monsoon season
- `'Oct-Dec'`: Post-monsoon season

## 📱 How to Use the Interactive Map

1. **Navigation**: Use the year slider to explore different time periods
2. **Animation**: Click the play button to automatically cycle through years
3. **Exploration**: Click on any marker to see detailed rainfall information
4. **Quick Info**: Hover over markers for instant tooltips
5. **Analysis**: Compare patterns across different years and seasons

