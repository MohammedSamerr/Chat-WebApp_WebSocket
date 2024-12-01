Spring Boot WebSocket Chat Application

A real-time chat application built with Spring Boot, WebSocket, and STOMP that allows users to send messages and get notified when a user joins or disconnects.

🚀 Features
Real-time Messaging: Send and receive messages instantly.
User Join Notifications: Broadcast a notification when a new user joins the chat.
User Disconnect Notifications: Alert all users when someone leaves the chat.
WebSocket with SockJS: Fall-back mechanism for WebSocket support in unsupported browsers.
Lightweight and Easy to Set Up: Just a few steps to get started with this project.
🛠️ Technologies Used
Backend: Spring Boot
Communication: WebSocket, STOMP, SockJS
Frontend: HTML, JavaScript, and SockJS Client
Template Engine: Thymeleaf (optional)
Logging: SLF4J with Logback (default)
📦 Installation & Setup
1. Clone the Repository
Clone the repository to your local machine:

git clone https://github.com/MohammedSamerr/Chat-WebApp_WebSocket.git
cd springboot-websocket-chat
2. Build the Project
If you're using Maven, run:

mvn clean install
If you're using Gradle, run:

gradle build
3. Run the Application
To start the application, run the following:

For Maven:
mvn spring-boot:run
For Gradle:
gradle bootRun
The application will be available at http://localhost:8080.

💡 How It Works
WebSocket Connection
Connect to WebSocket: Clients connect to the WebSocket server at /ws using SockJS for fallback support in unsupported browsers.
STOMP: The application uses the STOMP protocol to manage the messaging flow over WebSockets.
User Notifications: When a user joins or disconnects, a message is sent to the /topic/notifications channel that is broadcast to all connected users.
Message Handling: Messages sent by a user are forwarded to the /app/chat endpoint, which is then broadcast to all users via the /topic/messages channel.
🌍 Client-side Interaction
The client-side uses SockJS and STOMP to interact with the WebSocket server.

⚙️ How to Test
Open multiple browser tabs or windows.
Navigate to http://localhost:8080 in each tab.
When a user joins, you should see a notification in all open tabs about the new user.
Send a message, and it will be displayed in all connected clients.
When a user disconnects, the other clients will be notified of the disconnection.
📝 Contributing
We welcome contributions! If you'd like to contribute to this project, please follow these steps:

Fork this repository.
Create a new branch (git checkout -b feature-branch).
Commit your changes (git commit -am 'Add new feature').
Push to your branch (git push origin feature-branch).
Create a pull request.
📄 License
This project is licensed under the MIT License.

📈 Project Status
🚧 In Development – The application is currently being improved. You can contribute by submitting bug reports or feature requests.

🖼️ Screenshots
Here are a few screenshots of the chat application:

User Joining Notification

Real-time Chat