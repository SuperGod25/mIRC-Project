# mIRC Chat Application

This project is a simple chat application implemented using Java. It follows a client-server architecture, allowing multiple clients to communicate through a central server. Users can create channels, join existing ones, and broadcast messages within their selected channels.

## Features

- **Client-Server Architecture**: Clients communicate with a server using sockets.
- **Multiple Channels**: Users can create and connect to different chat channels.
- **User Authentication**: Basic user identification with usernames.
- **GUI Client**: The client application is built using `Swing` for the graphical user interface.

## Project Structure

The project is structured into three main packages:

- **Client**: Contains the client-side code that connects to the server.
  - `Client.java`: Handles the connection to the server and manages message sending/receiving.
  - `StartClient.java`: Creates the GUI interface and manages user interactions.
  
- **Server**: Contains the server-side code that handles multiple clients and channels.
  - `Server.java`: The main server class that manages connections, channels, and message broadcasting.
  - `StartServer.java`: Starts the server and listens for client connections.
  
- **Util**: Contains utility classes.
  - `User.java`: Defines the user model with a username.
  - `Channel.java`: Represents a chat channel with a name and password for joining.

## Getting Started

### Prerequisites

To run the project, ensure you have:

- Java 8 or higher installed on your system.
- An IDE like IntelliJ IDEA or Eclipse to open and run the project.

### Running the Server

1. Navigate to the `Server` package.
2. Run the `StartServer.java` class.
3. The server will start on `localhost` at port `2222`.

### Running the Client

1. Navigate to the `Client` package.
2. Run the `StartClient.java` class.
3. A GUI will appear, prompting you to enter a username and connect to the server.

### Commands

- **/connect `<channel_name>` `<password>`**: Join a channel with the specified name and password.
- **/create `<channel_name>` `<password>`**: Create a new channel with the given name and password.
- **/disconnect**: Disconnect from the current channel.

### Example Flow

1. Start the server by running `StartServer`.
2. Start one or more clients by running `StartClient`.
3. Enter a username on the client interface and click "Connect".
4. Use the input field to send messages or commands.

## Dependencies

- Java Swing for the GUI.
- Java Sockets for client-server communication.

## Future Enhancements

- Add encryption for secure message transmission.
- Implement user authentication with passwords.
- Improve UI with additional functionalities like message formatting, user lists, etc.

## License

This project is open-source and available under the [MIT License](LICENSE).
