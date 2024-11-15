
# WebRTC Encrypted Messaging Prototype
## _A Secure Messaging Application_

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/UnoSee)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project is a prototype for a secure messaging application using **WebRTC** for real-time peer-to-peer communication. It incorporates **end-to-end encryption (E2EE)** using `AES-GCM` to ensure that messages are encrypted before being sent and decrypted only by the intended recipient.

- Type messages securely between two peers.
- Messages are encrypted end-to-end.
- ✨ Real-time communication ✨

---

## Features

- **Real-time Messaging**: Send and receive messages instantly over WebRTC.
- **End-to-End Encryption**: Secure your communication with AES-GCM.
- **Key Sharing**: Uses Firebase Realtime Database to share encryption keys and signaling data.
- **Cross-Platform Compatibility**: Works on modern browsers like Chrome and Firefox.

---

## Tech Stack

This project uses the following open-source technologies:

- [React.js](https://reactjs.org/) - Frontend framework
- [Firebase](https://firebase.google.com/) - Realtime database for signaling
- [WebRTC](https://webrtc.org/) - Peer-to-peer communication
- [pnpm](https://pnpm.io/) - Fast, disk space-efficient package manager
- [TypeScript](https://www.typescriptlang.org/) - Type-safe development
- [AES-GCM](https://en.wikipedia.org/wiki/Galois/Counter_Mode) - Secure encryption algorithm

And of course, it uses **Node.js** as the runtime environment.

---

## Installation

Follow these steps to set up and run the application.

### Prerequisites

- **Node.js** v16+
- **pnpm** v8+ (Install globally if not already installed):
```bash
npm install -g pnpm
```
## Installation

### 1. Clone the repository
Start by cloning the repository to your local machine:

```bash
git clone https://github.com/UnoSee/Secure-Messenger.git
cd Secure-Messenger
```
### 2. Install dependencies
Use pnpm to install the required dependencies:
```bash
pnpm install
```
### 3. Set up Firebase
To enable signaling and key-sharing, you'll need to set up Firebase. If you don't have a Firebase account yet, you can create one at Firebase Console.

Once you have your Firebase project, follow these steps:
- Go to the Firestore Database section and create a new database.
- Go to the Realtime Database section and create a new database for storing signaling data and encryption keys.

Add the Firebase config to your .env file:
```bash
REACT_APP_FIREBASE_API_KEY=your-api-key
REACT_APP_FIREBASE_AUTH_DOMAIN=your-auth-domain
REACT_APP_FIREBASE_DATABASE_URL=your-database-url
REACT_APP_FIREBASE_PROJECT_ID=your-project-id
REACT_APP_FIREBASE_STORAGE_BUCKET=your-storage-bucket
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
REACT_APP_FIREBASE_APP_ID=your-app-id
```

### 4. Start the application
With everything set up, you can now start the application:
```bash
pnpm dev
```

## Usage
- Open the application in two separate tabs or different browsers to simulate two users.
- The first user can send a message to the second user by typing a message and hitting send.
- The messages are encrypted with AES-GCM before being sent over WebRTC.
- Only the second user can decrypt the message using the shared encryption key.

## Security Considerations
- End-to-End Encryption (E2EE) ensures that no one but the intended recipient can read the messages.
- WebRTC uses peer-to-peer communication, meaning messages don't go through centralized servers, reducing the risk of interception.
- AES-GCM provides both encryption and authentication, ensuring that the integrity of the message is maintained.
