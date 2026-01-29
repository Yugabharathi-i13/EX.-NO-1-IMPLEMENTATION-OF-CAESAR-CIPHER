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
int main() {
    char text[100], ch;
    int i, key;
    printf("Enter the plain text: ");
    scanf("%s", text);
    printf("Enter the key: ");
    scanf("%d", &key);
    printf("\n\nPlain text: %s",text);
    for(i = 0; text[i] != '\0'; i++) {
        ch = text[i];
        if(ch >= 'A' && ch <= 'Z') {
            ch = ((ch - 'A' + key) % 26) + 'A';
        }
        else if(ch >= 'a' && ch <= 'z') {
            ch = ((ch - 'a' + key) % 26) + 'a';
        }

        text[i] = ch;
    }
    printf("\nEncrypted/Cipher Text: %s",text);
    for(i = 0; text[i] != '\0'; i++) {
        ch = text[i];
        if(ch >= 'A' && ch <= 'Z') {
            ch = ((ch - 'A' - key + 26) % 26) + 'A';
            
        }
        else if(ch >= 'a' && ch <= 'z') {
            ch = ((ch - 'a' - key + 26) % 26) + 'a';
            
        }
        text[i] = ch;
        
    }
    printf("\nDecrypted Text: %s\n", text);
}
```

## OUTPUT:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/00e32aa7-9003-4bf8-9173-1d144e89b505" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
