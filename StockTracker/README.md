# GeoData Dashboard - User Guide

A React-based geospatial visualization dashboard for analyzing time-series data over interactive maps with polygon drawing and threshold-based coloring.

## 🚀 Quick Start

### Installation & Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the application:**
   ```bash
   npm run dev
   ```

3. **Open your browser:**
   - Navigate to `http://localhost:5000`
   - The dashboard will load automatically

### No API Keys Required!
This application uses the **Open-Meteo API**, which is completely free and requires no registration or API keys. You can start using it immediately.

---

## 📋 Dashboard Features Overview

### 🕒 Timeline Slider (Top Section)
**Purpose:** Control the time range for your data analysis

**How to use:**
- **Dual Range Handles:** Drag the blue handles to select start and end times
- **30-Day Window:** Shows 15 days before and 15 days after today
- **Play Controls:** 
  - ▶️ **Play:** Automatically advances time forward
  - ⏸️ **Pause:** Stops automatic time progression
  - ⏮️ **Previous:** Jump back one hour
  - ⏭️ **Next:** Jump forward one hour
  - 🔄 **Reset to Now:** Return to current time

**What it shows:**
- Current selected time range
- Duration in hours
- Date labels across the timeline

---

### 🗺️ Interactive Map (Main Section)
**Purpose:** Visualize spatial data and create analysis regions

**Drawing Tools (Right Panel):**
- 🖊️ **Draw Polygon:** Start creating a new polygon
- ✅ **Finish Drawing:** Complete your polygon (minimum 3 points)
- ❌ **Cancel Drawing:** Stop drawing and discard current polygon
- 🎯 **Center Map:** Return map to default position

**Map Features:**
- **Click to Draw:** When drawing mode is active, click on map to add points
- **Color-Coded Polygons:** Polygons change color based on temperature data
- **Fixed Zoom:** Locked at 2 sq. km resolution as specified
- **Real-time Updates:** Polygons automatically update when you change the timeline

**Drawing Rules:**
- Minimum: 3 points per polygon
- Maximum: 12 points per polygon
- Press **Enter** to finish drawing
- Press **Escape** to cancel drawing

---

### 📊 Sidebar (Left Panel)

#### Data Sources Section
**Purpose:** Configure how your data is visualized

**Features:**
- **Open-Meteo Integration:** Pre-configured weather data source
- **Active/Inactive Toggle:** Enable or disable data sources
- **Field Selection:** Choose what data to display:
  - Temperature (2m)
  - Relative Humidity (2m)
  - Surface Pressure

**Color Rules (Threshold-Based Coloring):**
- **Operators:** `<`, `≤`, `>`, `≥`
- **Values:** Set temperature thresholds
- **Colors:** Choose colors for each range
- **Example Rules:**
  - `< 10°C` → Red (Cold)
  - `≥ 10°C and < 25°C` → Blue (Medium)
  - `≥ 25°C` → Green (Warm)

**How to customize:**
1. Click color swatches to change colors
2. Adjust threshold values
3. Add new rules with "Add Rule" button
4. Delete rules with trash icon

#### Polygon Manager Section
**Purpose:** View and manage all created polygons

**Information Displayed:**
- **Polygon Name:** Auto-generated (Polygon 1, 2, etc.)
- **Points Count:** Number of vertices in the polygon
- **Current Value:** Live temperature reading
- **Color Indicator:** Shows current polygon color
- **Coordinates:** Center point of the polygon

**Actions:**
- 👁️ **Show/Hide:** Toggle polygon visibility
- ✏️ **Edit:** Modify polygon (coming soon)
- 🗑️ **Delete:** Remove polygon from map

---

## 🎯 How to Use the Dashboard

### Step 1: Set Your Time Range
1. Use the timeline slider to select when you want to analyze data
2. Drag the handles to set start and end times
3. Use play controls for automatic time progression

### Step 2: Draw Analysis Regions
1. Click the 🖊️ **Draw Polygon** button
2. Click on the map to add points (minimum 3, maximum 12)
3. Click ✅ **Finish Drawing** or press **Enter** when done
4. Your polygon will appear and automatically fetch temperature data

### Step 3: Customize Color Rules
1. In the sidebar, find the "Data Sources" section
2. Adjust the color thresholds to match your analysis needs
3. Choose different colors for different temperature ranges
4. Polygons will automatically update their colors

### Step 4: Analyze Your Data
1. Watch how polygon colors change as you move through time
2. View exact temperature values in the polygon manager
3. Create multiple polygons to compare different locations
4. Use the play feature to see temporal changes automatically

---

## 🎨 Understanding the Colors

The dashboard uses a **threshold-based coloring system**:

- **Default Setup:**
  - 🔴 **Red:** Temperatures below 10°C (Cold)
  - 🔵 **Blue:** Temperatures 10-25°C (Medium)
  - 🟢 **Green:** Temperatures above 25°C (Warm)

- **Custom Rules:** You can create your own color rules with any temperature thresholds and colors

---

## 🔧 Technical Details

### Data Source: Open-Meteo API
- **Free to use:** No registration required
- **Historical data:** Access to weather archives
- **Hourly resolution:** Detailed temporal data
- **Global coverage:** Works anywhere in the world

### Features Implemented
- ✅ 30-day sliding window timeline
- ✅ Interactive polygon drawing (3-12 points)
- ✅ Real-time data fetching from Open-Meteo
- ✅ Threshold-based color coding
- ✅ Automatic polygon color updates
- ✅ Sidebar management interface
- ✅ Play/pause timeline controls

### Keyboard Shortcuts
- **Enter:** Finish drawing polygon
- **Escape:** Cancel drawing polygon

---

## 🎓 Example Workflow

1. **Open the dashboard** - It loads with a default map centered on Berlin
2. **Set your time range** - Maybe select the last 5 hours using the timeline
3. **Draw a polygon** - Click draw tool, then click 4-5 points on the map around an area of interest
4. **Finish drawing** - Press Enter or click the finish button
5. **Watch it color** - The polygon will fetch temperature data and color itself
6. **Adjust time** - Drag the timeline handles to see how temperature changed over time
7. **Add more polygons** - Draw additional areas to compare different locations
8. **Customize colors** - Adjust the temperature thresholds to highlight specific ranges

---

## 💡 Tips for Best Results

- **Polygon Size:** Keep polygons reasonably sized for accurate data representation
- **Time Ranges:** Shorter time ranges provide more precise analysis
- **Color Rules:** Set thresholds that make sense for your local climate
- **Multiple Polygons:** Compare urban vs rural areas, or different elevations
- **Play Feature:** Use auto-play to quickly spot temporal patterns

---

## 🔍 Troubleshooting

**Polygon not showing data?**
- Check that your polygon has at least 3 points
- Ensure your time range includes valid historical data
- The Open-Meteo API provides data from recent years

**Colors not updating?**
- Verify your color rules are properly configured
- Check that the data source is active
- Try refreshing the page if data seems stuck

**Map not responding?**
- Make sure you've clicked the draw button before trying to draw
- Press Escape to cancel drawing mode if stuck

---

Ready to start exploring your geospatial data! 🌍