# Cryptography Work – RSA & AES Messaging

This Java project demonstrates how to encrypt and decrypt messages using a combination of RSA (for key exchange) and AES (for symmetric encryption). It includes simple client/server programs along with utilities for generating RSA keys, encrypting files, and signing/verifying messages.

## Features

- **RSA key generation** – create public/private key pairs using standard Java cryptography libraries.
- **AES encryption** – encrypt messages or files with a random symmetric key.
- **Hybrid encryption workflow** – encrypt the AES key using RSA so it can be securely shared between client and server.
- **Digital signatures** – sign encrypted messages with the sender’s private key and verify using the public key.
- **Client/server example** – simple Java programs demonstrating encryption, transmission and decryption between two parties.
- **Sample encrypted files** – example `.msg` files included to illustrate the encrypted outputs.

## Tech Stack

- **Language:** Java (JDK 8+)
- **Libraries:** Java Cryptography Architecture (JCA), javax.crypto
- **Build:** No external build tool required; compiled with `javac`
- **IDE support:** Works with IntelliJ IDEA, Eclipse or any standard Java IDE

## Project Structure

- `Client.java` / `Server.java` – example applications demonstrating sending encrypted messages.
- `RSAKeygen.java` – generates RSA key pairs.
- `batman.txt` – sample plaintext input file.
- `encrypted.msg` and `encrypted2.msg` – sample encrypted outputs.
- `sigC` / `sigS` – signature files for client and server.
- `server.prv` / `server.pub` – example private and public keys.

## Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/Timelaying/cryptography-work.git
   cd cryptography-work
   ```

2. **Compile the Java files**

   ```bash
   javac RSAKeygen.java Client.java Server.java
   ```

3. **Generate keys**

   ```bash
   java RSAKeygen
   ```
   This will create `server.prv` and `server.pub` in the current directory.

4. **Run the server**

   ```bash
   java Server
   ```

5. **Run the client in another terminal**

   ```bash
   java Client
   ```
   Follow the prompts to send and receive encrypted messages. The client reads `batman.txt` as input and produces encrypted output files.

## Usage Notes

- Make sure the client and server use the corresponding public/private keys for encryption and decryption.
- The sample code is for educational purposes and omits production-level error handling and security hardening.
- To clean up compiled class files, run `rm *.class`.

## Roadmap

- Add GUI for easier message entry and display.
- Use a build tool like Maven or Gradle with proper dependency management.
- Extend to support file encryption with larger file sizes.
- Add unit tests for cryptographic utilities.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
