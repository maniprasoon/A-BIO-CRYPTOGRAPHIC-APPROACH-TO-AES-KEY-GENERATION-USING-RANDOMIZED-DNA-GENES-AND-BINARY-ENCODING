# A-BIO-CRYPTOGRAPHIC-APPROACH-TO-AES-KEY-GENERATION-USING-RANDOMIZED-DNA-GENES-AND-BINARY-ENCODING

> A novel cryptographic key generation method that fuses biological entropy from DNA sequences with AES encryption using SHA-256, random sub-sequencing, and binary encoding.

## 📌 Overview

This project implements a **bio-cryptographic approach** to generate AES keys using randomized DNA gene sub-sequences and deterministic 6-bit binary identifiers. The combination is hashed using **SHA-256** to derive 256-bit AES keys, enabling secure data encryption and decryption with **CBC mode**.

## 🧬 Key Features

- 🧠 Bio-entropy based key generation using DNA sequences
- 🔐 AES encryption in Cipher Block Chaining (CBC) mode
- 🧮 SHA-256 hashing of DNA sub-sequences + binary identifiers
- 💾 No need for external key storage
- 📈 Microsecond-level timing analysis and performance visualization
- 🔄 Symmetric encryption with automatic base64 encoding for transport

## 🧪 Methodology

### 1. DNA Sub-sequence Generation
- Input: A reference DNA sequence
- Output: Random-length DNA sub-sequences paired with 6-bit binary identifiers

### 2. AES Key Generation
- Concatenate DNA sub-sequence + 6-bit binary ID
- Hash with SHA-256 → 256-bit AES key

### 3. AES Encryption
- AES-CBC mode with appropriate padding
- Converts cipher output to base64 for storage/transmission

### 4. AES Decryption
- Base64 decoded → decrypted using the same AES key

### 5. Timing Analysis
- Key generation times tracked using `time.perf_counter()`
- Visualized via line graph and microsecond precision stats

## 🔒 Example Output

- **DNA Sub-sequences**: `GCTA, CGTAGCTAGC, AGTAGCC, AC, TAGCTA`
- **Binary IDs**: `001111, 100011, 101011, 100000, 001000`
- **Generated Key (SHA-256)**: `24f6e344bf957f7f0de8dbf28f3762b65f94bbb6a40eb77e7a6a0b13e34cef46`
- **Encrypted Message**:  
  `IbIWGiReijompgcp/wLN+oW+VVCFVmcltBD8VVSL5tdFejR5Edaiian9AVfr6+S6`
- **Decrypted Message**:  
  `Hello, this is a test message!`

> Note: Output changes on every run due to randomized DNA sub-sequencing.

## 📊 Performance & Scalability

- Key generation time: **1.0–3.5 μs**
- Faster generation for shorter DNA sub-sequences
- Decryption optimized by sequence length
- Suitable for secure authentication and DNA-based key systems

## 🧭 Use Cases

- Secure medical data encryption
- Bio-personalized security systems
- DNA-driven authentication
- Quantum-resistant key generation approaches



