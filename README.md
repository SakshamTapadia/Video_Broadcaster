# Video Broadcaster with AI Background Customization 

![Demo Interface]
![image](https://github.com/user-attachments/assets/9c6de5bc-d00a-4aea-9439-2abb055131bc)



A sophisticated real-time video processing system using YOLOv8 segmentation for professional background manipulation. Now with enhanced UI/UX and performance optimizations.

## Major Updates ✨
- **New Modern UI**  
  Responsive design with device-adaptive layouts
- **Enhanced Error Handling**  
  User-friendly status updates and error messages
- **Improved Device Management**  
  Better camera detection and selection interface
- **Visual Feedback Controls**  
  Real-time blur strength indicator and button states
- **Performance Upgrades**  
  Expanded FPS range (1-1000) and optimized frame processing

## Key Features 🚀
```diff
+ New! Interactive range slider with live value display
+ Added loading states for buttons
+ Enhanced mobile responsiveness
+ Improved browser compatibility
```

## Installation Guide 📦

1. **Clone & Setup**
```bash
git clone https://github.com/username/sakshamtapadia-video-broadcaster.git
cd sakshamtapadia-video-broadcaster

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate    # Windows

# Install dependencies
pip install -r requirements.txt
```

2. **Add Required Assets**  
Place these files in `/static`:
- `logo.jpg` - Application logo
- `wallhaven.png` - Default background texture

## Launch Instructions 🖥️
```bash
python main.py
```
Access interface at `http://localhost:8000`

## Technical Enhancements ⚙️
| Component         | Improvements                          |
|-------------------|---------------------------------------|
| Frontend          | Modern CSS grid layout, SVG support   |
| Backend API       | Expanded FPS range, better validation |
| Error Handling    | Async operations with loading states  |
| Device Management | Smart camera detection algorithm      |

## Updated Project Structure 📂
```
sakshamtapadia-video-broadcaster/
├── LICENSE
├── README.md
├── engine.py           # Enhanced mask generation
├── main.py             # Improved API validation
├── stream_utils.py     # Optimized video pipeline
├── utils.py
├── yolov8m-seg.pt     # YOLOv8 segmentation model
└── static/
    ├── index.html     # Modernized UI
    ├── logo.jpg        # Application logo
    └── wallhaven.png  # Default background
```

## Configuration Matrix ⚙️
| Parameter        | Range         | Default | Description                |
|------------------|---------------|---------|----------------------------|
| `fps`            | 1-1000        | 15      | Output frame rate          |
| `blur_strength`  | 1-51 (odd)    | 21      | Background blur intensity  |
| `background`     | 3 options     | none    | Background replacement mode|

## Troubleshooting 🔧
**Common Issues:**
```bash
# Missing static assets
ERROR: 404 on /static/logo.jpg
SOLUTION: Ensure files exist in static/ directory

# Webcam not detected
ERROR: Camera list empty
SOLUTION: Check OS permissions for camera access

# Performance issues
SYMPTOM: Choppy video
FIX: Reduce FPS → Lower values (15-30) for slower hardware
```

## License 📄
MIT License - See [LICENSE](LICENSE) for full text

---

**Need Help?**  
Open an issue on GitHub with:
1. Error logs
2. Steps to reproduce
3. Device specifications

*Replace default background by modifying `static/wallhaven.png`*  
*Custom logo supported via `static/logo.jpg`*
