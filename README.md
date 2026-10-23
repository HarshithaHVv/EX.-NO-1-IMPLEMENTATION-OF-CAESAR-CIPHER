# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char text[100];
    int key, i;

    printf("Enter plaintext: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter key: ");
    scanf("%d", &key);

    key = ((key % 26) + 26) % 26;

    for (i = 0; text[i] != '\0'; i++) {
        if (isupper(text[i]))
            text[i] = (text[i] - 'A' + key) % 26 + 'A';
        else if (islower(text[i]))
            text[i] = (text[i] - 'a' + key) % 26 + 'a';
    }

    printf("Ciphertext: %s", text);

    return 0;
}
```


## OUTPUT:
<img width="1600" height="755" alt="WhatsApp Image 2026-10-23 at 9 26 47 AM (1)" src="https://github.com/user-attachments/assets/cad535fe-f561-4c1f-94ee-6c29c0ed9ac0" />



## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
