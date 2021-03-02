# Chapter 6

# 6-1
```c
#include <conio.h>
#include <stdio.h>
#include <math.h>
//Program to find the distance between two points

int u[2], v[2], dx, dy, dt;

int main(){
printf("Introduce the first vector. The x component and then y\n");
scanf("%d %d", &u[1], &u[2]);
printf("Now introduce the second one. The x component and then y\n");
scanf("%d %d", &v[1], &v[2]);
dx = v[1] - u[1];  
dy = v[2] - u[2];
dt = dx * dx + dy * dy;
dt = sqrt(dt);
printf("The distance between those vectors is %d", dt);
getch();
return 0;
}
```

# 6-2
```c
#include <conio.h>
#include <stdio.h>
//Program to give grades based on the percentage of correct answers
int c;
char g;

int main(){
printf("Introduce the percentage of correct answers\n");
scanf("%d", &c);
if (c >= 91){
	g = 'A';
}
else if (c >= 81){
	g = 'B';
}
else if (c >= 71){
	g = 'C';
}
else if (c >= 61){
	g = 'D';
}
else {
	g = 'E';
}
printf("The grade of this test is %c", g);
getch();
return 0;
}
```

# 6-3
```c
#include <conio.h>
#include <stdio.h>
//Program to give grades based on the percentage of correct answers and besides gives + or - based in the score
int c, a;
char g, s;

int main(){
printf("Introduce the percentage of correct answers\n");
scanf("%d", &c);
if (c >= 91){
	g = 'A';
}
else if (c >= 81){
	g = 'B';
}
else if (c >= 71){
	g = 'C';
}
else if (c >= 61){
	g = 'D';
}
else {
	g = 'E';
}
a = c % 10;
if (a >= 1 && a <=3){
	s = '-';
} 
else if (a >= 4 && a <=7){
	s = ' ';
}else{
	s = '+';
}
printf("The grade of this test is %c%c", g, s);
getch();
return 0;
}
```

# 6-4
```c
#include <conio.h>
#include <stdio.h>
// quarter 0.25  dime 0.10 nickel 0.05, penny .01
int v, q, d, n, rq, rd, rn;
int main(){
	printf("Introduce the value in cents (less than 1 dollar)\n");
	scanf("%d", &v);
	q = v / 25; // 25 cents     83   = 25*3=75
	rq = v % 25;  // read remaining of division of 25 cents =8
	d = rq / 10;  // 10 cents     =0
	rd = rq % 10;  // read remaining of division of 10 cents = 8
    n = rd / 05; // 5  cents = 1
	rn = rd % 05; //read remaining of division of 5 cents = 3
	
	printf("%d quarters\n%d dimes\n%d nickels\n%d pennies", q, d, n, rn);
	getch ();
	return 0;
}

```

# 6-5
```c
#include <stdio.h>
//Program to know wether a year is leap year or not
int y;
int main(){
printf("Introduce the year\n");
scanf("%d", &y);
if (y%4 == 0 && y%100 == 0 && y%400 == 0){
printf("%d is a leap year", y);
}
else if(y%4 == 0 && y%100 != 0 && y%400 != 0){
printf("%d is a leap year", y);
}else
{
	printf("%d is not a leap year", y);
}
return 0;
}
```

# 6-6
```c
#include <stdio.h>
//Program to know how many hours must be payed to an employee
float h, th, x;
int main(){
printf("Introduce the amount of hours worked in the week\n");
scanf("%f", &h);
if (h > 40){
x = h-40;
x = x*1.5;
th = h + x;
}
else{
th = h;
}
printf("You will be paid for working %.1f hours in total", th);
return 0;
}

```
