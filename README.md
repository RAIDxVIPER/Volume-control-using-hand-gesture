# Hand Gesture Volume Control

## Overview
This project enables users to control the system volume using hand gestures. It utilizes **OpenCV** for real-time hand tracking, **Mediapipe** for hand landmark detection, and **Pycaw** for audio control.

## Features
- Adjust system volume using finger distance
- Uses a green rectangle (detection box) to limit gesture recognition area
- Displays real-time volume percentage on the screen

## Requirements
Ensure you have the following installed:
- Python 3.x
- OpenCV (`cv2`)
- Mediapipe
- Pycaw (for audio control)

Install dependencies using:
```bash
pip install opencv-python mediapipe pycaw numpy comtypes
```

## Setup
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/hand-gesture-volume-control.git
   cd hand-gesture-volume-control
   ```
2. Run the script:
   ```bash
   python main.py
   ```

## Usage
1. The script will open a webcam window.
2. Place your hand inside the green rectangle (box) for detection.
3. Move your index finger and thumb closer or farther apart to adjust volume:
   - **Increase volume**: Spread fingers apart
   - **Decrease volume**: Bring fingers closer
4. The current volume percentage will be displayed on the screen.
5. Press `q` to exit.

## How It Works
- The script captures video from the webcam.
- It detects hand landmarks using **Mediapipe Hands**.
- If the index finger tip and thumb tip are inside the predefined green box, their distance is calculated.
- This distance is mapped to the system volume range using **Pycaw**.
- The volume is updated in real-time based on finger movements.

## Future Improvements
- Improve hand tracking accuracy
- Add gesture-based mute/unmute functionality
- Extend support for other media controls (e.g., play/pause)

## Contributing
Feel free to fork this repository and submit pull requests. Contributions are welcome!

## License
MIT License. See `LICENSE` for details.
