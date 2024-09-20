# RPS-with-CV
![🪨Rock_📄Paper_✂️ScissorsVSComputer(with_Computer_Vision)](https://github.com/user-attachments/assets/7b3aa1e8-58bc-4718-977c-ed8279bf9a16)

## Overview
This project is an interactive Rock Paper Scissors game that uses computer vision to detect hand gestures. Players can play against an AI opponent using their webcam, with real-time hand tracking and gesture recognition, an interactive GUI with multiple windows for game state, player choice, and AI choice, an AI opponent with randomized choices, Visual feedback for game progress and results.

## How It Works
1. **Hand Tracking**: Uses OpenCV and MediaPipe to capture and process webcam feed for hand detection.
2. **Gesture Recognition**: Analyzes hand landmarks by applying trig property Law of Cosines to calculate the angle of middle finger joints to detect if fingers are bent: all fingers bent is identified as rock pose, two fingers bent is identified as paper pose, and no fingers bent is identified as paper pose.
3. **Button Logic**: Draws button's onto webCamera using openCV's draw function, buttons can be hovered over with hand for set time to activate or "push"
4. **Game Logic**: Implements classic Rock Paper Scissors rules to determine the winner, the AI choice is decided with Python's random module.
5. **User Interface**: Utilizes Tkinter for creating multiple windows:
   - Main game window with webcam feed
   - Player's choice display
   - AI's choice display
   - Game state window for instructions and results

## Technical Stack
- Python 3.x
- OpenCV for image processing
- MediaPipe for hand tracking
- Tkinter for GUI
- Pillow for image handling

## Setup and Installation
1. Clone the repository
2. Install required packages:
```
pip install -r requirements.txt
```
3. Run the main Script

## How to Play
1. Launch the game and allow webcam access.
2. Hold your hand in front of the camera.
3. Make a Rock, Paper, or Scissors gesture when prompted.
4. The AI will make its choice, and the winner will be displayed.

## Future Improvements
1. Making it so the "ROCK" "PAPER" "SCISSORS" game state changes happen on the user's hand going up and then down again to increase interactivity and give the player more impact and responsiveness.
2. Adding pictures (possibly animations?) to the robot, GameStateWindow, and both the UserChoiceWindow and RobotChoiceWindow would make the game feel more real
3. It would be really cool to make the windows have a fly-in animation kind of like a pokemon battle start where the user window is a trainer and the computer is a trainer but I need to learn more about Tkinter and GUIs to make that possible (although I know it would be possible it would just take awhile to get it to fit the vision)
4. 

## Post Mortem
1. Creating a game through a webcam window and multiple GUI windows is inherently janky and hard to work with, would not recommend.
2. Such a high level of Python abstraction becomes much harder to work with and maintain + Code itself is messy and needs to be documented better in general.
3. The GUI could be much more clean and I suspect it wouldn't work properly on a different sized screen even though I tried my best to make it responsive to the screen size (although I haven't been able to test it).
