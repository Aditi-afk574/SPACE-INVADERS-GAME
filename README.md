# ADITI VISION ARCADE

### Gesture-Controlled Space Invaders using Computer Vision

A Python-based arcade game where the player controls a spaceship using hand gestures captured through a webcam. The project combines computer vision and real-time game development to create a touchless Space Invaders-style experience.

## Features

- Webcam-based hand tracking
- Horizontal hand movement to control the spaceship
- Gesture-based shooting
- Gesture-based ship flipping to target enemies in the opposite direction
- Real-time camera feed and gesture indicators
- Score and lives system
- Enemy formations, obstacles, lasers and sound effects

## Technology Stack

- **Python** - core application logic
- **OpenCV** - webcam capture and image processing
- **CvZone HandDetector** - hand tracking and finger detection
- **Pygame** - game window, sprites, events and audio
- **NumPy** - coordinate mapping and numerical operations

## Project Structure

```text
ADITI-VISION-ARCADE/
│
├── Code/
│   ├── main.py          # Starts and manages the game
│   ├── player.py        # Webcam, hand tracking and player controls
│   ├── alien.py         # Enemy sprites
│   ├── laser.py         # Laser behaviour
│   ├── obstacle.py      # Obstacle generation
│   └── requirements.txt # Python dependencies
│
├── Resources/           # Images, fonts and sound files
├── .gitignore
├── LICENSE
└── README.md
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/ADITI-VISION-ARCADE.git
cd ADITI-VISION-ARCADE
```

### 2. Create a virtual environment

**Windows PowerShell:**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, run:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```powershell
cd Code
python -m pip install -r requirements.txt
```

### 4. Run the game

```powershell
python main.py
```

> Allow camera access if Windows asks for permission.

## How It Works

```text
Webcam
  ↓
OpenCV Frame Capture
  ↓
CvZone Hand Detection
  ↓
Hand Landmarks / Finger States
  ↓
Gesture Logic
  ↓
Player Movement / Shoot / Flip
  ↓
Pygame Game Output
```

The webcam continuously captures frames. CvZone detects the hand and returns landmark and finger information. The program maps the hand position to the spaceship and checks the detected finger pattern to trigger game actions.

## Controls

The exact gesture behaviour follows the implementation in `Code/player.py`.

- **Move:** Move your hand horizontally
- **Shoot:** Use the shooting gesture configured in the current player code
- **Flip:** Use the flip gesture configured in the current player code

## Troubleshooting

**`main.py` not found**

Make sure you are inside the `Code` folder before running the program:

```powershell
cd Code
python main.py
```

**Camera opens briefly and closes**

Check the terminal for the first Python error. Also make sure no other application is using the webcam.

**Module not found**

Activate `.venv` and run:

```powershell
python -m pip install -r requirements.txt
```

## Author

**Aditi Tandon**

College Project | Computer Vision | Gesture Control | Arcade Game Development

## Credits and Attribution

This project was developed as a modified and customized version of an existing open-source gesture-controlled arcade game. The original repository and contributors are credited under the included MIT License. The project also uses concepts and the CvZone hand-tracking module associated with Murtaza's Workshop, and builds on general Pygame Space Invaders tutorial concepts credited by the original project.

The original MIT copyright notice and license are retained in `LICENSE`.

## License

This repository retains the included **MIT License** and its required copyright notice.


## Project Presentation

The project presentation is available in the `Presentation/` folder:

- `Aditi_Vision_Arcade_Presentation.pptx`
