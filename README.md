# Network Library for Unity3D

![Unity](https://img.shields.io/badge/Unity-3D-blue.svg) ![License](https://img.shields.io/badge/License-MIT-green.svg) ![OpenSource](https://img.shields.io/badge/Open-Source-blue.svg)

A powerful and easy-to-use network library for Unity3D that provides robust TCP and UDP communication. Designed for simplicity and flexibility, this library ensures smooth networking for multiplayer games and applications.

## Features
- **TCP & UDP Communication**: Supports both protocols for reliable and fast data transfer.
- **Factories for Easy Setup**: Quick and straightforward setup process.
- **Server & Client Wrappers**: Includes auto-reconnect and auto-join functionalities.
- **Object-Oriented Approach**: No need to deal with raw bytes, send and receive objects directly.
- **RSA Encryption**: Optional encryption for both TCP and UDP communication.
- **Multiple Communication Methods**: Use lambdas, delegates, or async operations for sending and receiving objects.
- **Quick Info Transmission**: Send small pieces of information without creating objects.
- **Logging & Debugging Tools**: Built-in logging for monitoring network traffic and debugging.
- **No Magic Numbers**: No need for identifiers or complex configurations.
- **Fast, Reliable & Customizable**: High-performance and flexible code for various use cases.
- **Clean & Understandable Code**: Written in easy-to-read C# for better maintainability.
- **Open Source & Free to Use**: Licensed under MIT, freely available for everyone.

## Installation
1. Clone or download the repository:
   ```sh
   git clone https://github.com/attributeyielding/Network-Library-For-Unity-3D.git
   ```
2. Add the library to your Unity project.
3. Start implementing networking using the provided API.

## Usage
### Setting Up a Server
```csharp
TcpServer server = new TcpServer(12345);
server.Start();
```

### Setting Up a Client
```csharp
TcpClient client = new TcpClient("127.0.0.1", 12345);
client.Connect();
```

### Sending an Object
```csharp
client.Send(new MyData { message = "Hello, Server!" });
```

### Receiving an Object
```csharp
server.OnDataReceived += (sender, data) => {
    MyData received = data as MyData;
    Console.WriteLine(received.message);
};
```

## Contribution
We welcome contributions! Feel free to submit issues or pull requests to improve the library.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
For any questions or support, open an issue on the repository.

Happy coding! 🚀

