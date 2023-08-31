<h1>RSA/AES Encryption</h1>

This repository contains Java code examples for encryption using two different encryption algorithms: AES (Advanced Encryption Standard) and RSA (Rivest–Shamir–Adleman).


<h2>AES (Advanced Encryption Standard)</h2>

AES is a symmetric encryption algorithm, meaning the same key is used for both encryption and decryption. It operates on fixed-size blocks of data and is highly efficient. The following steps outline how AES encryption works:

1. **Key Generation**: A secret encryption key is generated. In the provided code, a 128-bit key is used.

2. **Encryption**:
   - The plaintext message is divided into fixed-size blocks.
   - AES operates on these blocks using various transformations (substitution, permutation, mixing, and XOR operations).
   - A unique initialization vector (IV) is used to add randomness to each encryption operation, preventing patterns.
   - The encrypted message, along with authentication tag and IV, is produced.

3. **Decryption**:
   - The encrypted message is divided into blocks.
   - Using the same key and IV, AES performs inverse transformations to retrieve the original plaintext message.

AES provides efficient and fast encryption suitable for large amounts of data.

<h2>RSA (Rivest–Shamir–Adleman)</h2>

RSA is an asymmetric encryption algorithm, utilizing a pair of keys: public and private keys. It's often used for secure key exchange and digital signatures. Here's a high-level overview of RSA encryption:

1. **Key Generation**: A key pair is generated - a public key for encryption and a private key for decryption. The key sizes are typically larger (e.g., 2048 bits) to ensure security.

2. **Encryption**:
   - The recipient's public key is used for encryption.
   - The plaintext is converted into a numeric value.
   - The plaintext value is raised to the power of the recipient's public exponent and then modulo the public modulus to obtain the ciphertext.

3. **Decryption**:
   - Only the private key holder can decrypt the ciphertext.
   - The ciphertext value is raised to the power of the private exponent and then modulo the private modulus to retrieve the original numeric value.
   - The numeric value is then converted back into plaintext.

RSA provides a secure method for data transmission, digital signatures, and key exchange.


