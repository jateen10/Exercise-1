# Exercise<br>
## task 1<br>
### Algorithm<br>
step 1:intialize i= 0<br>
 step 2:for i=0 i, i greater equal to 30, i increment<br>
 step 3:if i divisible by 5 and i divisable 3<br>
             print vaule ("fizzbuzz")<br>
step 4: else if i divisible by 5:<br>
             print value ("buzz") <br>
step 5:else if i divisible by 3:<br>
             print vaule ("fizz")<br>
step 6: print value (i)<br>
stop<br>

### code in pyton<br>
 for i in range ( 1 ,30):<br>
 if i %5 ==0, $ i % 3==0:<br>
 print("fizzbuzz<br>
 elsif i % 5 == 0:<br>
 print("fizzz"):<br>
  elsif i % 3 == 0<br>
 print("buzz")<br>
 print (i)<br>

<br>
## task 2<br>
### Algorithm<br>
Convert numbers to Ordinal words Algorithm<br>
strt <br>
step 1 :create a function Num-to-words with pararmeters number and output<br>
step 2 : inside the function create an if statement such that if the number is 0 <br>
the result will be "zeroth"<br>
step 3 : create 4 arrays<br>
   array 1 contains all numbers from 1 to 9 in words <br>
   array 2 contains all numbers multiple of 10  from 10 to 90 in words <br>
   array 3 contains all numbers from 1 to 9 in ordinal words <br>
   array 4 contains all numbers multiple of 10 from 10 to 90 in ordinal words<br>
step 4 : create nested if statement such that if number is modulo divisible by 10 the digit is in ones place and so on<br>
step 5 : create nested if statements such that if the digit is in hundreds place output the digit from array 1 and 2 followed by the word hundred and
so on for thousands, millions etc<br>
step 6 : create an if statement such that if the digit is in tens places and the digit in 0nes place is zero <br>
output the coressponding value from  array 3<br><br>
else if the digit in ones place is not zero and the digit at tens place is a non zero output<br>
the coressponding value from array2 and 4<br>
step 7 : return return output <br>
step 8: take the input for parameter number from the user and call the function Num-To-words<br>
print the entered number <br>
output<br><br>
stop<br>
### code in c++<br>
#include <stdio.h><br>
#include <string.h><br>
<br>

char *single_digits[] = { “zero”, “one”, “two”, “three”, “four”,”five”,”six”, “seven”, “eight”, “nine”};<br>

char *two_digits[] = {“”, “ten”, “eleven”, “twelve”, “thirteen”, “fourteen”,”fifteen”, “sixteen”,”seventeen”, “eighteen”, “nineteen”};<br>

char *tens_multiple[] = {“”, “”, “twenty”, “thirty”, “forty”, “fifty”,<br>
“sixty”, “seventy”, “eighty”, “ninety”};<br>

char *tens_power[] = {“hundred”, “thousand”};<br>
/* single number*/<br>
<br>if (len == 1) {
<br>printf(“%s\n”, single_digits[*num – ‘0’]);
<br>return;<br>
}
<br>
<br>while (*num != ‘\0’) {
<br>if (len >= 3) {
<br>if (*num -‘0’ != 0) {
<br>printf(“%s “, single_digits[*num – ‘0’]);
<br>printf(“%s “, tens_power[len-3]); // here len can be 3 or 4
}
<br>–len;
}
<br>
<br>/* Code for last 2 digits */
<br>else {
<br>if (*num == ‘1’) {
<br>int sum = *num – ‘0’ + *(num + 1)- ‘0’;
<br>printf(“%s\n”, two_digits[sum]);
<br>return;
}
<br>else if (*num == ‘2’ && *(num + 1) == ‘0’) {
<br>printf(“twenty\n”);
<br>return;
}
<br>
<br>/* number range 21 to 99 */
<br>else {
<br>int i = *num – ‘0’;
<br>printf(“%s “, i? tens_multiple[i]: “”);
<br>++num;
<br>if (*num != ‘0’)
<br>printf(“%s “, single_digits[*num – ‘0’]);
<br>}
<br>}
<br>++num;
<br>}
<br>}
<br>
<br>int main(void)
<br>{
<br>char a[10];
<br>printf(“\nEnter the number : “);
scanf(“%s”,a);
<br>printf(“\nThe number in word is “);
<br>convert(a);
<br>return 0;
<br>}
