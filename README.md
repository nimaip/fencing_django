# Fencing Pose Analysis (Django)

A Django-based web application for analyzing fencing poses using computer vision and pose estimation with OpenCV and MediaPipe.

## Features

- **En Garde Pose Analysis**: Analyzes the en garde stance for proper form
- **Lunge Pose Analysis**: Analyzes the lunge position for correct technique
- **Real-time Feedback**: Provides detailed feedback on pose angles and positioning
- **Visual Annotations**: Shows annotated images with pose landmarks and angles
- **Angle Calculations**: Measures knee, elbow, and spine angles for precise feedback

## Installation

1. **Install Python dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Run the application**:
   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

3. **Open your browser** and go to:
   ```
   http://localhost:8000
   ```

## Usage

1. Select the pose type (En Garde or Lunge)
2. Upload an image of your fencing pose
3. Click "Analyze Pose" to get detailed feedback
4. View the original and annotated images with analysis results

## Technical Details

- **Backend**: Django web framework
- **Computer Vision**: OpenCV and MediaPipe for pose detection
- **Frontend**: HTML, CSS
- **Image Processing**: Real-time pose analysis with angle calculations

## File Structure

```
fencing_django/
├── fencing_app/
│   ├── views.py           # Main Django views (real analysis)
│   └── urls.py            # App URLs
├── fencing_project/
│   ├── settings.py        # Django settings
│   ├── urls.py            # Project URLs
│   └── wsgi.py            # WSGI entry point
├── enGarde.py             # En garde pose analysis
├── lunge.py               # Lunge pose analysis
├── manage.py              # Django management script
├── requirements.txt       # Python dependencies
├── static/
│   └── css/
│       └── style.css      # Custom styles
└── templates/
    └── index.html         # Main HTML template
```

## Dependencies

- Django 5.0.2
- OpenCV 4.9.0.80
- MediaPipe 0.10.8
- NumPy 1.26.4
- Pillow 10.2.0
- python-dotenv 1.0.1

## Notes

- This version performs real pose analysis with OpenCV and MediaPipe
- Images are processed in memory and not permanently stored
- Maximum file size is 16MB
- Requires a local environment that supports OpenCV and MediaPipe dependencies
