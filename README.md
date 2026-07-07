Basketball Video Analysis
An app that analyzes basketball game footage to track players and the ball automatically, assign players to teams, and surface key game events.
Demo: https://youtu.be/EKy758zMkoc
How it works
The pipeline runs footage through several detection models: one YOLO-based model finds and tracks the ball, another tracks players across frames, and a third detects court keypoints (lines, corners, key zones) to understand where on the court the action is happening. Once players are tracked, jersey colors are used to automatically assign each player to a team. From there, the system determines ball possession frame-by-frame and flags passes and interceptions as they happen. Bounding boxes, court lines, and event overlays are drawn directly onto the output video, producing a fully annotated version of the original footage.
Models can either be trained from scratch on custom datasets (training notebooks included) or loaded from pretrained weights for faster setup. The app runs via a simple command-line entry point, taking in a raw video file and producing an annotated output video.
