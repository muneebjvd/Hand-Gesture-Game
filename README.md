# Hand-Gesture-Game
Video Feed Capture: The game uses camera_utils.js to continuously stream real-time frames from your webcam directly into the MediaPipe processing engine.
Hand Landmark Tracking: The MediaPipe Hands machine learning model tracks 21 skeletal points on your hand, focusing specifically on the Index Finger Tip and the Wrist.
Mirrored Steering Control: It translates the horizontal coordinate of your index finger tip into the game canvas space, inverting it so that moving your hand right moves the car right.
Input Smoothing (lerp): The code applies linear interpolation (lerp) to the coordinates, filtering out camera noise to ensure the car moves smoothly rather than jittering.
Fist Detection: It continuously calculates the pixel distance between your index finger tip and your wrist. If they get close enough (under 60 pixels), it registers a fist to start or restart the game.
Game Loop & Collision: The p5.js engine updates the game states, spawns obstacles, tracks your score, and uses bounding-box math to end the game if an obstacle hits your car.
