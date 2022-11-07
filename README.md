# Exercise
## task 1
### Algorithm
step 1:intialize i= 0
 step 2:for i=0 i, i greater equal to 30, i increment
 step 3:if i divisible by 5 and i divisable 3
             print vaule ("fizzbuzz")
step 4: else if i divisible by 5:
             print value ("buzz") 
step 5:else if i divisible by 3:
             print vaule ("fizz") 
step 6: print value (i)
stop

### code in pyton
 for i in range ( 1 ,30):
 if i %5 ==0, $ i % 3==0:
 print("fizzbuzz")
 elsif i % 5 == 0:
 print("fizzz"):
  elsif i % 3 == 0:
 print("buzz")
 print (i)


## task 2
### Algorithm
Convert numbers to Ordinal words Algorithm
strt
step1:create a function Num-to-words with pararmeters number and output
step2: inside the function create an if statement such that if the number is 0 
the result will be "zeroth"
step3: create 4 arrays
   array1 contains all numbers from 1 to 9 in words 
   array2 contains all numbers multiple of 10  from 10 to 90 in words 
   array3 contains all numbers from 1 to 9 in ordinal words 
   array4 contains all numbers multiple of 10 from 10 to 90 in ordinal words
step4: create nested if statement such that if number is modulo divisible by 10 the digit is in ones place and so on
step5: create nested if statements such that if the digit is in hundreds place output the digit from array 1 and 2 followed by the word hundred and 
so on for thousands, millions etc
step6: create an if statement such that if the digit is in tens places and the digit in 0nes place is zero 
output the coressponding value from  array 3
else if the digit in ones place is not zero and the digit at tens place is a non zero output
the coressponding value from array2 and 4
step7: return return output 
step8: take the input for parameter number from the user and call the function Num-To-words
print the entered number 
output
stop
### code in c++
#include <stdio.h>
#include <string.h>


char *single_digits[] = { “zero”, “one”, “two”, “three”, “four”,”five”,”six”, “seven”, “eight”, “nine”};

char *two_digits[] = {“”, “ten”, “eleven”, “twelve”, “thirteen”, “fourteen”,”fifteen”, “sixteen”,”seventeen”, “eighteen”, “nineteen”};

char *tens_multiple[] = {“”, “”, “twenty”, “thirty”, “forty”, “fifty”,
“sixty”, “seventy”, “eighty”, “ninety”};

char *tens_power[] = {“hundred”, “thousand”};
/* single number*/
if (len == 1) {
printf(“%s\n”, single_digits[*num – ‘0’]);
return;
}

while (*num != ‘\0’) {
if (len >= 3) {
if (*num -‘0’ != 0) {
printf(“%s “, single_digits[*num – ‘0’]);
printf(“%s “, tens_power[len-3]); // here len can be 3 or 4
}
–len;
}

/* Code for last 2 digits */
else {
if (*num == ‘1’) {
int sum = *num – ‘0’ + *(num + 1)- ‘0’;
printf(“%s\n”, two_digits[sum]);
return;
}
else if (*num == ‘2’ && *(num + 1) == ‘0’) {
printf(“twenty\n”);
return;
}

/* number range 21 to 99 */
else {
int i = *num – ‘0’;
printf(“%s “, i? tens_multiple[i]: “”);
++num;
if (*num != ‘0’)
printf(“%s “, single_digits[*num – ‘0’]);
}
}
++num;
}
}

int main(void)
{
char a[10];
printf(“\nEnter the number : “);
scanf(“%s”,a);
printf(“\nThe number in word is “);
convert(a);
return 0;
}
