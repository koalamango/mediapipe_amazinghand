# [MediaPipe](https://github.com/google-ai-edge/mediapipe) + [AmazingHand](https://github.com/pollen-robotics/AmazingHand)

Real-time browser-based hand tracking, sending finger movements to AmazingHand over WebSocket.

<!-- Add a demo video here. -->

Original code reference: [Seeed Studio – AmazingHand MediaPipe Hand Tracking Demo](https://wiki.seeedstudio.com/hand_amazinghand/#mediapipe-hand-tracking-demo)

## Quick Start

Install Python dependencies:

```
python3 -m pip install websockets pyserial numpy rustypot
```

### Set the USB serial port

Open `hand_tracking.py` and set
`SERVO_CONTROLLER_PORT` to the port for Amazing Hand:

```
SERVO_CONTROLLER_PORT = "<Local_USB Serial_Port_Number>"
```

## Run Hand Tracking

Start both servers in separate terminals. Run each command from the project
folder and leave both terminals open.

```
  python3 hand_tracking.py
```

The server listens on
`ws://127.0.0.1:8765`.

Open second terminal, start the local web server:

```
python3 -m http.server 8000
```

Open <http://localhost:8000> in your browser and allow webcam access.

## Mediapipe Hand Landmarks

![hand-landmarks](hand-landmarks.png)
