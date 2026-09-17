📘 PRACTICAL – 4
CRYPTOGRAPHY

🎯 Aim

To study different cryptographic techniques such as encryption, hashing, and digital signatures, understand their applications, and implement them using suitable cryptographic tools.

📝 Introduction

Cryptography is the technique of protecting information by converting it into a form that cannot be easily understood by unauthorized users.

It is widely used in cybersecurity, online banking, e-commerce, messaging applications, digital payments, and secure communication.

The main objectives of cryptography are:

🔒 Confidentiality
       ↓
🛡️ Integrity
       ↓
👤 Authentication
       ↓
✍️ Non-Repudiation

🔐 1. Encryption

Encryption converts readable data, known as plaintext, into an unreadable form called ciphertext using an algorithm and a key.

The ciphertext can be converted back into plaintext through decryption using the appropriate key.

Basic Process
Plaintext
    ↓
Encryption + Key
    ↓
Ciphertext
    ↓
Decryption + Key
    ↓
Plaintext

Types of Encryption
Symmetric Encryption
The same key is used for encryption and decryption.

Examples:

AES

ChaCha20

             Same Key
          ↙            ↘
Plaintext → Encryption → Ciphertext
                         ↓
                     Decryption
                         ↓
                      Plaintext

Asymmetric Encryption
A key pair is used:

Public key

Private key

Examples include RSA and elliptic-curve cryptography.

Public Key
    ↓
Encryption
    ↓
Ciphertext
    ↓
Private Key
    ↓
Decryption

#️⃣ 2. Hashing

Hashing converts data into a fixed-length value called a hash or digest.

Unlike encryption, a cryptographic hash is designed to be one-way; it is not intended to be decrypted back into the original data.

Common cryptographic hash functions include:

SHA-256

SHA-384

SHA-512

Hashing Process
Original Data
      ↓
Hash Function
      ↓
Fixed-Length Hash

Example
Input
  ↓
"Hello World"
  ↓
SHA-256
  ↓
Hash Value

Hashing is commonly used for:

Password verification

File integrity checking

Digital signatures

Data integrity verification

✍️ 3. Digital Signature

A digital signature is a cryptographic mechanism used to help verify the authenticity and integrity of digital information.

It uses a private key to create a signature and a corresponding public key to verify it.

Digital Signature Process
Original Message
       ↓
   Hash Function
       ↓
   Message Hash
       ↓
Private Key + Hash
       ↓
Digital Signature

The recipient can use the sender's public key and the relevant verification process to check whether the signature is valid.

Digital signatures are commonly used for:

Electronic documents

Software distribution

Digital certificates

Secure communications

Online transactions

🛠️ Cryptographic Tools

Some commonly used tools and technologies include:

Tool / Technology	Purpose
OpenSSL	Encryption, hashing, certificates and digital signatures
GnuPG (GPG)	Encryption and digital signatures
Python Cryptography Libraries	Implementing cryptographic operations
SHA-256	Cryptographic hashing
AES	Symmetric encryption
RSA / ECC	Public-key cryptography

💻 Practical Implementation

A simple cryptography exercise can be performed using Python.

Example: SHA-256 Hashing
import hashlib

message = "Hello World"

hash_value = hashlib.sha256(message.encode()).hexdigest()

print("Original Message:", message)
print("SHA-256 Hash:", hash_value)

Output

Original Message: Hello World
SHA-256 Hash: <generated hash value>

The same input produces the same SHA-256 digest, while even a small change to the input produces a substantially different digest.

🔄 Comparison of Techniques
Feature	Encryption	Hashing	Digital Signature
Main purpose	Confidentiality	Integrity	Authenticity & integrity
Reversible?	Yes, with appropriate key	No, by design	Signature is verified, not decrypted
Uses keys?	Yes	No key required for basic hashing	Yes
Common examples	AES, ChaCha20	SHA-256	RSA/ECDSA signatures
Typical use	Protecting data	Verifying data	Signing documents/software

🔒 Cryptography in Cybersecurity

Cryptography can be represented as:

                 CRYPTOGRAPHY
                      │
        ┌─────────────┼─────────────┐
        ↓             ↓             ↓
   Encryption      Hashing    Digital Signature
        │             │             │
 Confidentiality   Integrity    Authentication

These techniques can work together to provide multiple layers of security.

⚠️ Important Security Practices

When implementing cryptography:

Use established, well-reviewed algorithms.

Avoid creating your own cryptographic algorithms.

Protect private keys carefully.

Use strong, randomly generated keys.

Use secure password-hashing methods for passwords rather than plain SHA-256.

Keep cryptographic libraries updated.

Never expose private keys or secret keys unnecessarily.

📋 Practical Checklist
[✓] Study encryption
[✓] Understand symmetric encryption
[✓] Understand asymmetric encryption
[✓] Study cryptographic hashing
[✓] Study digital signatures
[✓] Explore cryptographic tools
[✓] Implement a basic hashing example
[✓] Compare cryptographic techniques
[✓] Understand real-world applications

✅ Result

Different cryptographic techniques, including encryption, hashing, and digital signatures, were studied. Their purposes, working principles, applications, and differences were examined, and a basic SHA-256 hashing implementation was demonstrated.

🏁 Conclusion

Cryptography is an important component of modern cybersecurity. Encryption helps protect confidentiality, hashing helps verify data integrity, and digital signatures help establish authenticity and integrity. Understanding these techniques provides a foundation for developing and using secure information systems.



