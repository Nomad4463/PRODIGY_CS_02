# Pixel Swapping Encryption and Decryption Tool

This Python tool allows you to encrypt and decrypt images using pixel swapping techniques. You can choose to encrypt an image, decrypt it, or perform both operations in sequence.
This can also be done using Caeser Cipher encyption [Caeser cipher git](https://github.com/Nomad4463/PRODIGY_CS_01)

## Features

- **Encrypt Images:** Rearrange pixels in an image using a generated swap map.
- **Decrypt Images:** Restore the original image by reversing the pixel swaps.
- **Interactive User Input:** Choose to encrypt, decrypt, or both. Provide a seed to ensure reproducibility.

## Requirements

- Python 3.x
- Pillow library (Python Imaging Library)

Install the Pillow library using pip:

```bash
pip install pillow
```

## Usage

### 1. Encrypt an Image

To encrypt an image, run the script and follow the prompts:

```bash
python image_swap_encryptor.py
```

#### Prompts

- **Choose an operation:** Enter `ENCRYPT` to encrypt the image.
- **Enter the seed:** Provide a numeric seed (e.g., `42`). This seed will be used to generate the swap map.
- **Optional:** After encryption, you will be asked if you want to decrypt the image. Enter `yes` to decrypt or `no` to skip.

### 2. Decrypt an Image

To decrypt an image, ensure you have the seed used for encryption:

```bash
python image_swap_encryptor.py
```

#### Prompts

- **Choose an operation:** Enter `DECRYPT` to decrypt an image.
- **Enter the seed used for encryption:** Provide the seed that was used during encryption to generate the correct swap map.

### 3. Perform Both Operations

To automatically encrypt and then decrypt an image:

```bash
python image_swap_encryptor.py
```

#### Prompts

- **Choose an operation:** Enter `BOTH` to perform encryption followed by decryption.
- **Enter the seed:** Provide a numeric seed (e.g., `42`). This seed will be used for both operations.

## Example

### Encrypt and Decrypt

```plaintext
Choose an operation (ENCRYPT, DECRYPT, BOTH): ENCRYPT
Enter the seed (an integer): 42
Do you want to decrypt the image? (yes/no): yes
```

### Decrypt Only

```plaintext
Choose an operation (ENCRYPT, DECRYPT, BOTH): DECRYPT
Enter the seed used for encryption: 42
```

### Both Operations

```plaintext
Choose an operation (ENCRYPT, DECRYPT, BOTH): BOTH
Enter the seed (an integer): 42
```

## File Paths

- **Input Image:** `input_image.jpg` (replace with your image file)
- **Encrypted Image:** `encrypted_image.png`
- **Decrypted Image:** `decrypted_image.jpg`

## Notes

- Ensure the input image exists in the same directory as the script, or update the file path accordingly.
- The seed value must be the same for encryption and decryption to correctly restore the original image.
- The swap map is generated randomly based on the seed, so using the same seed will yield consistent results.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

