# EX 4 : ELLIPSE DRAWING ALGORITHM

NAME : REXLIN R

REG NO: 212222220034

**AIM :**


To  implement the Bresenham’s  algorithm for ellipse using a c coding.


**EQUIPMENT REQUIRED:**


●	Hardware: Personal Computer (PC)


●	Software: C Compiler

**ALGORITHM :**

Step 1 : Start.
  
Step 2 : Initialize the graphics header files and functions.
   
Step 3 : Declare the required variables and functions.
 
Step 4 : Get the co-ordinates and radius of the ellipse.

Step 5 : Draw the ellipse using the algorithm.

Step  6 : Display the output.
 
Step 7 : stop.


**Program :**

```
#include "stdio.h" 
#include "conio.h" 
#include "math.h" 
#include "graphics.h" 
main() 
{ 
  int gd=DETECT,gm; 
  int xcenter,ycenter,rx,ry; 
  int p,x,y,px,py,rx1,ry1,rx2,ry2; 
  initgraph(&gd,&gm,"c:\\turboc3\\bgi");
  printf("Enter The Radius Value:\n"); 
  scanf("%d%d",&rx,&ry); 
  printf("Enter The xcenter and ycenter Values:\n"); 
  scanf("%d%d",&xcenter,&ycenter); 
  ry1=ry*ry; 
  rx1=rx*rx; 
  ry2=2*ry1; 
  rx2=2*rx1; 
x=0; 
  y=ry; 
  plotpoints(xcenter,ycenter,x,y); 
  p=(ry1-rx1*ry+(0.25*rx1)); 
  px=0; 
  py=rx2*y; 
  while(px<py) 
  { 
   x=x+1; 
   px=px+ry2; 
   if(p>=0) 
    y=y-1; 
    py=py-rx2; 
 
 
    if(p<0) 
     p=p+ry1+px; 
    else 
     p=p+ry1+px-py; 
  plotpoints(xcenter,ycenter,x,y); 
 
 
 
 
 
p=(ry1*(x+0.5)*(x+0.5)+rx1*(y-1)*(y-1)-rx1*ry1);
while(y>0)
  { 
   y=y-1; 
   py=py-rx2; 
   if(p<=0) 
   { 
    x=x+1; 
    px=px+ry2; 
            } 
                     if(p>0) 
    p=p+rx1-py; 
   else 
    p=p+rx1-py+px; 
               plotpoints(xcenter,ycenter,x,y); 
          } 
      } 
  getch(); 
  return(0); 
            } 
 
int plotpoints(int xcenter,int ycenter,int x,int y) 
{ 
  putpixel(xcenter+x,ycenter+y,6); 
  putpixel(xcenter-x,ycenter+y,6); 
  putpixel(xcenter+x,ycenter-y,6); 
  putpixel(xcenter-x,ycenter-y,6);
  return 0;
 
}
```


**Output :**

![ellipsegamedevlopment](https://github.com/user-attachments/assets/51b06629-23d3-4109-91e3-f236dba53d95)


**Result :**

Thus the Bresenham’s  algorithm for ellipse using a c coding is implemented successfully .
