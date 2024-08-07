# Simple Image Encryption Tool

This repository contains a basic image encryption and decryption tool using pixel manipulation. The tool leverages simple mathematical operations to encrypt and decrypt images. This project is intended for educational purposes and basic obfuscation of images.

## Features

- **Simple Encryption:** Uses XOR operation on each pixel's RGB values with a user-defined key.
- **Decryption:** Reverses the encryption using the same key to restore the original image.
- **Supports Common Image Formats:** Works with various image formats like JPEG, PNG, etc.

## Getting Started

### Prerequisites

Ensure you have Python installed. You'll also need the Pillow library for image processing.

Install the required dependencies:

```bash
pip install pillow
```

### Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/image-encryption-tool.git
cd image-encryption-tool
```

2. Encrypt an image:

```python
from image_encryptor import encrypt_image

key = 42  # Define your encryption key
encrypt_image("input_image.jpg", "encrypted_image.png", key)
```

3. Decrypt the image:

```python
from image_encryptor import decrypt_image

decrypt_image("encrypted_image.png", "decrypted_image.jpg", key)
```

### Example

```python
from image_encryptor import encrypt_image, decrypt_image

key = 42  # Simple XOR key

# Encrypt the image
encrypt_image("input_image.jpg", "encrypted_image.png", key)

# Decrypt the image
decrypt_image("encrypted_image.png", "decrypted_image.jpg", key)
```

### File Structure

```plaintext
image-encryption-tool/
│
├── image_encryptor.py  # Contains the encryption and decryption functions
├── README.md           # This readme file
└── requirements.txt    # Python dependencies
```

### Security Considerations

This encryption method is very basic and not secure for sensitive data. It's intended for educational purposes or simple obfuscation only. For more secure image encryption, consider using established cryptographic libraries.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
