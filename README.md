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


Usage
const PolygonSplitter = require('polygon-splitter');

const polygon = [[0,0],[10,0],[10,10],[0,10],[0,0]]; // must be closed
const polyline = [[5,-1],[5,11]];

const [polyA, polyB] = PolygonSplitter.split(polygon, polyline);

console.log('Polygon A:', polyA);
console.log('Polygon B:', polyB);


API
PolygonSplitter.split(polygon, polyline)

polygon: Array of [x, y] points, must be closed (first point = last point)

polyline: Array of [x, y] points, at least 2 points

returns: [PolygonA, PolygonB] — two closed polygons

Other internal methods (for reference):

_validateInput(poly, cutter)

_approxEqual(a, b, eps)

_closePolygon(p)

_pointInPolygon(pt, poly)

_pointOnSegment(p, a, b, eps)

_lineIntersection(A, B, C, D)

_interpPoint(A, B, poly)

_insertPoints(poly, pin, pout)
