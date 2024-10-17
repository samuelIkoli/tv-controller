Slide Control with Flutter and NodeJS via WebSocket
This project allows you to control a Slideshow (or any other software) remotely, simulating mouse and keyboard movements through a Flutter application connected via WebSocket to a NodeJS server. The Flutter app uses the device's accelerometer and gyroscope sensors to detect movements, providing a fluid experience for navigating between slides or performing actions remotely.

Features
Remote control of slideshows.
Simulation of mouse movements and keyboard actions.
Real-time connection between NodeJS and Flutter application via WebSocket .
Using accelerometer and gyroscope sensors to detect movements.
Ideal for those who need to control presentations while away from their device.
Requirements
Server (NodeJS)
Node.js (v14.x or higher)
WebSocket
Libraries for mouse and keyboard simulation
Application (Flutter)
Flutter SDK (v2.0 or higher)
Plugin sensors_plusfor accessing device sensors
WebSocket for communication with the server
Installation
1. Clone the repository
git clone https://github.com/cl0v/tv-controller
cd tv-controller
2. NodeJS Server Configuration
Install NodeJS dependencies:

cd nodejs
npm install
3. Start the WebSocket Server
node main.js
4. Flutter App Setup
Make sure Flutter is installed and dependencies are configured:

cd flutter
flutter pub get
5. Run the Flutter App
Connect a device or use the emulator to run the app:

flutter run
How it Works
NodeJS Server
The NodeJS server receives commands from the Flutter application via WebSocket and simulates mouse and keyboard actions on the host system. Depending on the data sent by the accelerometer and gyroscope, the server performs the following actions:

Mouse Movement : Based on device tilt and movement.
Slide Forward/Backward : Using device-specific gestures or tilts to send keyboard commands (e.g., seta para esquerdaand keys seta para direita).
Flutter App
The application collects motion data through sensors (accelerometer/gyroscope) and sends this data to the NodeJS server via WebSocket. The server interprets this data and transforms it into mouse/keyboard commands.

Usage Examples
Left/Right Movement
Tilt the device to the left to simulate pressing the left arrow key .
Tilt the device to the right to simulate pressing the right arrow key .
Mouse Movement
Smooth movements on the X or Y axis of the gyroscope can be used to move the mouse cursor.
Screenshots
Usage example

Technologies Used
NodeJS : To manage WebSocket server and control mouse and keyboard actions.
WebSocket : For real-time communication between the server and the Flutter app.
Flutter : To capture accelerometer and gyroscope data and send to server.
sensors_plus : Flutter plugin to access sensors like the accelerometer and gyroscope.
robotjs : NodeJS library to simulate mouse and keyboard actions.
Contributing
Fork the project
Create a branch for your feature ( git checkout -b feature/nova-feature)
Commit your changes ( git commit -m 'Adiciona nova feature')
Push to the branch ( git push origin feature/nova-feature)
Open a Pull Request
Buy me a Coffee
Give a ⭐️ if this project helped you!


License
This project is licensed under the Apache License 2.0 .

Contact
If you have any questions or suggestions, feel free to open an issue or contact us via LinkedIn .

Project Structure:
nodejs/ : Contains the NodeJS server code.
flutter/ : Contains the Flutter application code.
