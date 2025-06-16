# SilhouetteForge - Freemium Version

## Description
SilhouetteForge is a Python application for converting silhouette images into 3D printable STL files. This is the Freemium version with limited functionality.

## Freemium Features

### License Limitations
- **3 generations without watermark** per week
- **5 total generations with watermark** per week
- Automatic weekly counter reset
- Automatic watermark when non-watermark generations are exhausted
- **No stands** generated (available in higher versions)

### Main Features
- ✅ Image loading (PNG, JPG, JPEG, BMP)
- ✅ Automatic contour detection
- ✅ 3D model generation with customizable thickness
- ✅ 2D preview of detected contours
- ✅ Integrated 3D viewer (if OpenGL available)
- ✅ STL file export
- ✅ Configurable watermark system
- ✅ Remaining generations counter
- ✅ Startup splash screen
- ✅ Futuristic Material Design interface

### License Controls
- Watermark switch (forced when necessary)
- Visible generations counter
- Upgrade popup when limits reached
- License upgrade links
- Print ordering links

## Installation

### Prerequisites
```bash
pip install -r requirements.txt
```

### Main Dependencies
- `opencv-python` - Image processing
- `numpy` - Numerical calculations
- `trimesh` - 3D mesh generation
- `shapely` - 2D geometry
- `PyQt5` - Graphical interface

### Optional Dependencies
- `PyOpenGL` - 3D viewer (if not available, it will be disabled)

## Usage

1. **Application Startup**
   ```bash
   python src/main.py
   ```

2. **Image Loading**
   - Click "Load Image"
   - Select a silhouette image

3. **Parameter Configuration**
   - **Image Threshold**: Binarization threshold (default: 128)
   - **Min Contour Area**: Minimum contour area (default: 1000.0)
   - **3D Thickness**: 3D model thickness (default: 5.0mm)

4. **Model Generation**
   - Choose whether to add watermark
   - Click "Generate 3D Model"
   - View 3D preview (if available)

5. **Export**
   - Click "Export STL"
   - Choose save path

## File Structure

```
SilhouetteForge/
├── src/
│   └── main.py              # Main application
├── assets/
│   └── logo.ico             # Application icon
├── requirements.txt         # Python dependencies
└── README.md               # Documentation
```

## License Configuration

Configuration is saved in:
- **Windows**: `%USERPROFILE%\.silhouetteforge\config.json`
- **Linux/Mac**: `~/.silhouetteforge/config.json`

### Configuration Structure
```json
{
  "license_type": "freemium",
  "weekly_generations": 0,
  "weekly_watermark_generations": 0,
  "week_start": "2024-01-01T00:00:00",
  "max_weekly_generations": 3,
  "max_weekly_watermark_generations": 5
}
```
## Future Features
- Website for purchasing licenses and prints
- Development of Standard, Pro and Commercial versions

## License Versions

### 🆓 Freemium (Current)
- 3 generations/week without watermark
- 5 generations/week with watermark
- No stands

### 💼 Standard
- Unlimited generations
- Private license (non-commercial)
- Stands included

### 🚀 Pro
- Unlimited generations
- Commercial license
- Stands with multiple styles

### 🏢 Commercial
- All Pro features
- 15 free prints/month
- Access to premium print forms

## Troubleshooting

### OpenGL Not Available
```
OpenGL not available. 3D viewer will be disabled.
```
**Solution**: Install PyOpenGL or continue without 3D viewer

### CSS Errors
```
Unknown property box-shadow
```
**Note**: Normal PyQt5 warnings, do not affect functionality

### Contour Errors
- Verify that the image has sufficient contrast
- Adjust the "Image Threshold" value
- Ensure the minimum contour area is appropriate

## Support

- **License Upgrade**: https://silhouetteforge.com/upgrade
- **Order Prints**: https://silhouetteforge.com/order-prints

## Technical Notes

- The application automatically saves usage statistics
- Weekly reset occurs automatically
- Watermarks are applied only to the preview, not to the 3D model
- 3D generation preserves the original conversion logic
- The interface maintains the original Material Design style
