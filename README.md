# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## NAME : YUGABHARATHI T
## REG.NO : 212224040375

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
int main() {
    char text[100], ch;
    int i, key;
    printf("Enter the plain text: ");
    scanf("%s", text);
    printf("Enter the key: ");
    scanf("%d", &key);

    printf("\nPlain text: %s", text);
    for(i = 0; text[i] != '\0'; i++) {
        ch = text[i];
        if(ch >= 'a' && ch <= 'z') {
            ch = ch - 32;
        }
        if(ch >= 'A' && ch <= 'Z') {
            ch = ((ch - 'A' + key) % 26) + 'A';
        }
        text[i] = ch;
    }
    printf("\nCipher Text/Encrypted Text: %s", text);
    for(i = 0; text[i] != '\0'; i++) {
        ch = text[i];

        if(ch >= 'A' && ch <= 'Z') {
            ch = ((ch - 'A' - key + 26) % 26) + 'A';
        }

        text[i] = ch;
    }
    printf("\nDecrypted Text: %s\n", text);
}

```

## OUTPUT:
<img width="1690" height="968" alt="image" src="https://github.com/user-attachments/assets/674ebfe5-9883-4b0e-85b0-b54e2da6bed1" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
