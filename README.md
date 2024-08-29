# ft_irc

An Internet Relay Chat (IRC) server implementation project developed as part of the 42 school curriculum. This project aims to create a functional IRC server that follows the IRC protocol, enhancing understanding of network programming, socket communication, and server-client architecture.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [IRC Commands](#irc-commands)
- [TODO List](#todo-list)
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

## TODO List

1. Network Setup
   - [ ] Implement socket creation and binding
   - [ ] Set up listening for incoming connections
   - [ ] Handle client connections using select() or poll()

2. Client Handling
   - [ ] Implement client data structure
   - [ ] Manage client authentication
   - [ ] Handle client disconnections

3. Message Parsing
   - [ ] Develop a robust parser for IRC messages
   - [ ] Implement command recognition

4. Command Implementation
   - [ ] NICK command
   - [ ] USER command
   - [ ] JOIN command
   - [ ] PART command
   - [ ] PRIVMSG command
   - [ ] QUIT command
   - [ ] MODE command
   - [ ] TOPIC command
   - [ ] LIST command
   - [ ] NAMES command

5. Channel Management
   - [ ] Implement channel data structure
   - [ ] Manage user joining and leaving channels
   - [ ] Handle channel modes

6. Message Routing
   - [ ] Implement message broadcasting to channels
   - [ ] Handle private messages between users

7. Error Handling
   - [ ] Implement proper error responses as per IRC protocol
   - [ ] Handle edge cases and potential issues

8. Configuration
   - [ ] Implement server configuration (port, password)
   - [ ] Optional: Configuration file support

9. Logging
   - [ ] Implement server-side logging for debugging and monitoring

10. Testing
    - [ ] Develop a comprehensive test suite
    - [ ] Perform stress testing with multiple clients

Bonus Tasks:
- [ ] Implement file transfer functionality
- [ ] Create a basic IRC bot

## Contributing

This project is part of the 42 school curriculum. While contributions are not expected, feel free to fork the project for your own learning and experimentation.

## License

This project is licensed under the GNU Affero General Public License v3.0 (AGPLv3) - see the [LICENSE](LICENSE) file for details. This license ensures that the code remains open source and that any modifications or distributions of the code also remain open source, in line with the 42 school philosophy.
