- Certificate:
- caPublicKey: 
- govPublicKey: 
- HKDF: Key derivation function
- DH key exchange => use ElGamal key pairs (generateEG)
- Symmetric encryption algorithms (sending & receiving keys) => AES-GCM
- Header of sent msgs includes: 
    + enc of sending key under govPublicKey
    + IV

- Every clients => ElGamal key pair
    + pk: distributed through certificates

- Generate a new random IV every time encrypt with AES-GCM (genRandomSalt())