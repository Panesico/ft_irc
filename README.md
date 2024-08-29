# ft_irc

An Internet Relay Chat (IRC) server implementation project developed as part of the 42 school curriculum. This project aims to create a functional IRC server that follows the IRC protocol, enhancing understanding of network programming, socket communication, and server-client architecture.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [IRC Commands](#irc-commands)
- [Program Flow](#program-flow)
- [Module Division and TODO List](#module-division-and-todo-list)
- [Contributing](#contributing)
- [License](#license)

## Installation

```bash
git clone https://github.com/Panesico/ft_irc.git
cd ft_irc
make
```

## Usage

To run the IRC server:

```bash
./ircserv <port> <password>
```

Where:
- `<port>` is the port number on which your IRC server will listen for incoming connections
- `<password>` is the connection password

## Features

- TCP socket programming
- Client-server communication
- Multiple client handling
- Channel management
- User authentication
- Message routing between clients and channels
- Implementation of IRC commands

Bonus features (if implemented):
- File transfer
- Bot integration

## IRC Commands

The ft_irc server typically implements the following IRC commands:

1. `NICK`: Set or change nickname
2. `USER`: Set username, hostname, and realname
3. `JOIN`: Join a channel
4. `PART`: Leave a channel
5. `PRIVMSG`: Send a private message to a user or channel
6. `QUIT`: Disconnect from the server
7. `MODE`: Change user or channel modes
8. `TOPIC`: View or set a channel topic
9. `LIST`: List available channels
10. `NAMES`: List users in a channel

Usage examples:

```
/NICK newNickname
/JOIN #channel
/PRIVMSG #channel :Hello, everyone!
/PART #channel
/QUIT :Goodbye!
```

## Program Flow

Here's a high-level overview of how the program should flow:

1. Server Initialization
   - Create and bind socket
   - Set socket to non-blocking mode
   - Start listening for connections

2. Main Event Loop
   - Use select() or poll() for non-blocking I/O
   - Accept new client connections
   - Receive data from existing clients
   - Parse received messages
   - Route messages to appropriate command handlers
   - Send responses back to clients

3. Command Handling
   - Process specific IRC commands
   - Update server state (e.g., user information, channel memberships)
   - Generate and send appropriate responses

4. Client Disconnection
   - Handle client disconnections (voluntary or due to errors)
   - Clean up resources associated with disconnected clients

5. Server Shutdown
   - Close all client connections
   - Free allocated resources
   - Close server socket

## Module Division and TODO List

The project is divided into three main modules, each with its own set of tasks:

### 1. Network and Client Management Module

- **Socket Management and Initialization**
   - [ ] Implement socket creation and binding
   - [ ] Set up listening for incoming connections
   - [ ] Set up non-blocking I/O using select() or poll()
   - [ ] Implement basic error handling and logging for network operations

- **Client Management**
   - [ ] Implement client data structure
   - [ ] Handle client connections (accept new clients)
   - [ ] Manage client connections and disconnections
   - [ ] Handle multiple clients concurrently
   - [ ] Implement the main event loop

### 2. Message Parsing and Command Handling Module

- **Message Parsing**
   - [ ] Implement IRC protocol message parser
   - [ ] Route messages to appropriate handlers

- **Command Handling**
   - [ ] Implement NICK command
   - [ ] Implement USER command
   - [ ] Implement JOIN command
   - [ ] Implement PART command
   - [ ] Implement PRIVMSG command
   - [ ] Implement QUIT command
   - [ ] Implement MODE command
   - [ ] Implement TOPIC command
   - [ ] Implement LIST command
   - [ ] Implement NAMES command
   - [ ] Generate and format server responses
   - [ ] Implement error handling for invalid commands or parameters

### 3. Channel and Server State Management Module

- **Channel Management**
   - [ ] Implement channel data structure
   - [ ] Handle channel creation and deletion
   - [ ] Manage channel user lists

- **Server State Management**
   - [ ] Implement server-wide state management (users, channels, etc.)
   - [ ] Handle client authentication
   - [ ] Manage client nickname and username changes
   - [ ] Integrate networking module for sending responses
   - [ ] Integrate command handling module for executing commands
   - [ ] Implement final error handling and logging system
   - [ ] Coordinate overall program flow
   - [ ] Implement server shutdown procedure

### Additional Features (Optional, can be distributed among team members)

- [ ] Implement file transfer functionality
- [ ] Create a bot interface

## Contributing

This project is part of the 42 school curriculum. While contributions are not expected, feel free to fork the project for your own learning and experimentation.

## License

This project is licensed under the GNU Affero General Public License v3.0 (AGPLv3) - see the [LICENSE](LICENSE) file for details. This license ensures that the code remains open source and that any modifications or distributions of the code also remain open source, in line with the 42 school philosophy.
