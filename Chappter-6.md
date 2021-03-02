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