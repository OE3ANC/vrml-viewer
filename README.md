# VRML Viewer

A lightweight custom HTML element for displaying VRML files in the browser using ThreeJS

## Quick Start

```html
<!DOCTYPE html>
<html>
<head>
    <title>VRML Viewer</title>
</head>
<body>
    <vrml-viewer src="board.wrl.gz" width="800" height="600"></vrml-viewer>

    <script type="importmap">
    {
        "imports": {
            "three": "https://cdn.jsdelivr.net/npm/three@0.160.1/build/three.module.js",
            "three/addons/": "https://cdn.jsdelivr.net/npm/three@0.160.1/examples/jsm/"
        }
    }
    </script>
    
    <script type="module" src="src/vrml-viewer.js"></script>
</body>
</html>
```

**Start local server:** `python3 -m http.server 8000`

## Attributes

| Attribute | Default | Description |
|-----------|---------|-------------|
| `src` | - | Path to VRML file (.wrl or .wrl.gz) |
| `width` | 800 | Viewer width in pixels |
| `height` | 600 | Viewer height in pixels |
| `background-color` | "#f8f8f8" | Background color |
| `responsive` | false | Enable responsive sizing |


## JavaScript API

```javascript
const viewer = document.querySelector('vrml-viewer');

// Load a model
await viewer.load('path/to/model.wrl.gz');

// Clear the current model
viewer.clear();

// Reset camera view
viewer.resetView();
```

