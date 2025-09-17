# PolygonSplitter

## English

### Overview
`PolygonSplitter` is a lightweight Node.js utility class for splitting polygons using polylines. It provides a simple, intuitive API to process polygon geometries in 2D space. Perfect for GIS, mapping, or CAD-related projects that need polygon cutting logic without heavy dependencies.

### Features
- Split a closed polygon with a polyline
- Handles point-in-polygon detection
- Automatically inserts intersection points on polygon edges
- Returns two resulting polygons after the split
- Pure JavaScript, no external dependencies

### Installation
```bash
# Clone the repository
git clone https://github.com/cosiu1994-debug/PolygonSplitter.git
cd PolygonSplitter

# Or install via npm if published
npm install polygon-splitter
