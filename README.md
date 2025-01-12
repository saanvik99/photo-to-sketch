# Photo-to-Sketch
A Flask module that converts photos into artistic pencil sketches using OpenCV. This module is designed to be integrated into a larger Flask application and provides image processing capabilities with a user-friendly web interface.


## Features

- Convert photos to pencil sketch style drawings
- Support for multiple image formats (PNG, JPG, JPEG, GIF, BMP)
- Real-time preview of conversions
- Gallery view of converted images
- Downloadable results
- Error handling and input validation
- Automatic image resizing for large uploads

## Module Structure

```
app/modules/photo_to_sketch/
├── __init__.py           # Module initialization
├── image_processor.py    # Core image processing logic
├── sketch_service.py     # Service layer for business logic
└── routes.py            # Route definitions and request handling

app/templates/modules/photo_to_sketch/
├── convert.html         # Main conversion page
└── gallery.html        # Gallery view template

app/static/modules/photo_to_sketch/
├── css/
│   └── sketch_styles.css
└── js/
    └── sketch_main.js

## Prerequisites

- Python 3.8+
- OpenCV (cv2)
- NumPy
- Pillow
- Flask

## Installation

1. Ensure the module is in your Flask application's modules directory:
```bash
app/modules/photo_to_sketch/
```

2. Install required dependencies:
```bash
pip install opencv-python numpy pillow flask
```

3. Register the blueprint in your Flask application:
```python
from app.modules.photo_to_sketch import photo_to_sketch

app.register_blueprint(photo_to_sketch)

### Gallery
- `GET /photo-to-sketch/gallery`
  - Displays gallery of converted images
  - Shows thumbnails and download links



