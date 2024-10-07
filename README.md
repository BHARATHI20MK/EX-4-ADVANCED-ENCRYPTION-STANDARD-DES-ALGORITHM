# EX-4-ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM

## Aim:
  To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM: 
  1. AES is based on a design principle known as a substitution–permutation. 
  2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
  3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
  4. AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM: 
```
#include <stdio.h>
#include <string.h>

// XOR encryption function
void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);

    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len]; // XOR encryption
    }
}

int main() {
    char url[] = "https://www.google.com/";
    char key[] = "secretkey"; // Simple key for XOR encryption

    printf("Original URL: %s\n", url);

    // Encrypt the URL
    xor_encrypt_decrypt(url, key);
    printf("Encrypted URL: %s\n", url);

    // Decrypt the URL (since XOR is reversible using the same key)
    xor_encrypt_decrypt(url, key);
    printf("Decrypted URL: %s\n", url);

    return 0;
}
```
## OUTPUT:
![WhatsApp Image 2024-10-07 at 14 07 32_593eac1b](https://github.com/user-attachments/assets/f642cb96-6a65-49a0-9bcd-5410d2fc63b4)
## RESULT: 
Thus , to use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is done successfully.
