# Try

#include <stdio.h>
#include <math.h>
int main()
{
    int counter,f_coun;
    float sum=0,x,power,fact;
    printf("equation series : 1- X^2/2! + X^4/4! - X^6/6! + X^8/8! - X^10/10!");
    printf("\nenter value of X : ");
    scanf("%f",&x);
    for(counter=0, power=0; power<=10; counter++,power=power+2)
    {
        fact=1;
                for(f_coun=power; f_coun>=1; f_coun--)
            fact *= f_coun;
        sum=sum+(pow(-1,counter)*(pow(x,power)/fact));
    }
    printf("Sum : %f",sum); 
}



#Palandorime number: 

#include <string.h>
int isPalindrome(char str[]);
int main() {
 char inputString[100];
 printf("Enter a string: ");
 gets(inputString);
 if (isPalindrome(inputString)) {
 printf("%s is a palindrome.\n", inputString);
 } else    {
 printf("%s is not a palindrome.\n", inputString);           }
 return 0;     }
int isPalindrome(char str[]) {
 int i, length = strlen(str);
 for (i = 0; i < length / 2; i++) {
 if (str[i] != str[length - i - 1]) {
 return 0; 
 }
 }
 return 1; 
}
