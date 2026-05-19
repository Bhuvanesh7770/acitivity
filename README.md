Attendance assignment
1. Write a program to read a string and count the number of vowels using a separate function.
#include <stdio.h>

int countVowels(char str[]) {
    int count = 0;
    for(int i = 0; str[i] != '\0'; i++) {
        char ch = str[i];
        if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||
           ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U') {
            count++;
        }
    }
    return count;
}

int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);

    printf("Number of vowels = %d", countVowels(str));
    return 0;
}
output:
Enter a string: hello
Number of vowels = 2
2. Write a function to reverse a string without using library functions like strrev().
#include <stdio.h>

void reverse(char str[]) {
    int len = 0;
    while(str[len] != '\0') len++;

    for(int i = len-1; i >= 0; i--) {
        printf("%c", str[i]);
    }
}

int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);

    printf("Reversed string: ");
    reverse(str);

    return 0;
}
output:
Enter a string: hello
Reversed string: olleh
3. Write a program to check whether a given string is palindrome or not using functions.
#include <stdio.h>

int isPalindrome(char str[]) {
    int len = 0;
    while(str[len] != '\0') len++;

    for(int i = 0; i < len/2; i++) {
        if(str[i] != str[len-i-1]) {
            return 0;
        }
    }
    return 1;
}

int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);

    if(isPalindrome(str))
        printf("Palindrome");
    else
        printf("Not Palindrome");

    return 0;
}
output:
Enter a string: madam
Palindrome
4. Write a function to calculate the length of a string manually.
#include <stdio.h>

int length(char str[]) {
    int count = 0;
    while(str[count] != '\0') {
        count++;
    }
    return count;
}

int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);

    printf("Length = %d", length(str));
    return 0;
}
output:
Enter a string: hello
Length = 5
5. Write a function to count the number of words in a sentence.
#include <stdio.h>

int countWords(char str[]) {
    int count = 0;

    for(int i = 0; str[i] != '\0'; i++) {
        if(str[i] == ' ')
            count++;
    }
    return count + 1;
}

int main() {
    char str[100];
    printf("Enter a sentence: ");
    getchar();
    fgets(str, sizeof(str), stdin);

    printf("Number of words = %d", countWords(str));
    return 0;
}
output:
Enter a sentence: I love coding
Number of words = 3
