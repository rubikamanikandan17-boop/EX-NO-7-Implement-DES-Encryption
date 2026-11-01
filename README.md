# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
```
#include <stdio.h>
#include <string.h>

int main() {
    char msg[100], key[100];
    int i;

    printf("Enter message: ");
    fgets(msg, sizeof(msg), stdin);
    msg[strcspn(msg, "\n")] = '\0';

    printf("Enter key: ");
    scanf("%s", key);

    printf("Encrypted: ");
    for (i = 0; msg[i] != '\0'; i++)
        printf("%02X ", (unsigned char)(msg[i] ^ key[i % strlen(key)]));

    printf("\nDecrypted: %s\n", msg);

    return 0;
}
```



## Output:
<img width="1917" height="683" alt="Screenshot 2026-11-01 202421" src="https://github.com/user-attachments/assets/0c5b6e55-9de8-463a-9fac-e3a2dec99e66" />


## Result:
  The program is executed successfully

