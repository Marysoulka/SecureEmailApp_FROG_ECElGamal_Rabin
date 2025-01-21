# Secure Email Exchange Application

This project demonstrates a secure email exchange system, integrating **encryption-decryption using FROG in CFB mode**, **secure key delivery with Elliptic Curve El-Gamal**, and **digital signing using the Rabin signature algorithm**. The system ensures confidentiality, integrity, and authenticity in email communication.


## Overview

In today’s digital communication landscape, ensuring data security is paramount. This project combines state-of-the-art cryptographic techniques to create a secure email exchange system. By leveraging both symmetric and asymmetric encryption algorithms alongside digital signature verification, it addresses potential vulnerabilities in electronic messaging.

## Features

1. **Symmetric Encryption with FROG in CFB Mode**:
   - Encrypts email messages block by block.
   - Uses an Initialization Vector (IV) to enhance randomness.
   - Ensures data confidentiality and efficient encryption for large datasets.

2. **Asymmetric Encryption with Elliptic Curve El-Gamal**:
   - Provides secure key exchange for symmetric encryption.
   - Uses smaller keys for equivalent security, improving performance.

3. **Digital Signatures with Rabin**:
   - Verifies the authenticity of the sender.
   - Ensures message integrity, preventing unauthorized alterations.


## How It Works
### Message Flow:
1. **Sender (Alice)**:
   - Encrypts the email message using the FROG algorithm in CFB mode.
   - Generates a digital signature for the encrypted message using the Rabin signature algorithm.
   - Encrypts the symmetric encryption key using Elliptic Curve El-Gamal.
   - Sends the encrypted message, encrypted key, public key for EC El-Gamal, and digital signature to the recipient.

2. **Receiver (Bob)**:
   - Verifies the Rabin digital signature to ensure authenticity.
   - Decrypts the symmetric encryption key using EC El-Gamal.
   - Decrypts the email message using the FROG algorithm and the decrypted key.


## Technologies Used

- **Python**: Cryptographic algorithms and testing framework.
- **FROG Algorithm**: Block-based symmetric encryption.
- **Elliptic Curve El-Gamal**: Asymmetric encryption for secure key delivery.
- **Rabin Signature Algorithm**: Digital signature generation and verification.

## Repository Contents

- **`code/`**:
  - Implementation of FROG encryption in CFB mode, EC El-Gamal, and Rabin signature.
  - Test cases to validate encryption, decryption, and signature verification.
  
- **`presentation/`**:
  - A PowerPoint file presenting the project architecture, algorithms, and implementation.

## Challenges

Throughout the development process, the team faced several challenges, including:

1. **Optimization of Cryptographic Algorithms**:
   - Implementing the FROG algorithm with minimal overhead while maintaining security.
   - Efficiently handling large datasets for encryption and decryption.

2. **Asymmetric Key Management**:
   - Generating and verifying EC El-Gamal keys for secure key delivery.

3. **Digital Signature Verification**:
   - Ensuring Rabin signatures were efficiently generated and correctly verified under various conditions.

## Conclusion

This project successfully demonstrates a secure and efficient email exchange system. By integrating robust cryptographic methods, it achieves:

- **Confidentiality**: The FROG encryption algorithm ensures that only the intended recipient can access the message content.
- **Integrity**: The Rabin signature validates the authenticity and integrity of the message.
- **Secure Key Delivery**: Elliptic Curve El-Gamal ensures the symmetric encryption key is safely transmitted.

This system showcases the effectiveness of combining symmetric and asymmetric encryption with digital signatures to create a comprehensive secure communication framework.
