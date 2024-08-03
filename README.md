1. Program to assign two integer values to X and Y. Using the 'if' statement the output of the program should display a message whether X is greater than Y.

import java.io.*;

public class Lab1

{

public static void main (String []args) throws IOException
{

int x,y;

DataInputStream ds = new DataInputStream(System.in);
System.out.println("Enter X and Y value");

x = Integer.parseInt(ds.readLine());

y = Integer.parseInt(ds.readLine());

if(x > y)

System.out.println(" Largest is X with value "+x);
if(y>x)

System.out.println(" Largest is Y with value "+y);
}

}


2 Program to list the factorial of the numbers 1 to 10. To calculate the factorial value, use while loop. (Hint Fact of 4 = 4*3*2*1)

import java.io.*;

public class Lab2

{

public static void main(String []args) throws IOException
{

int ans, i, j;

for( i=1; i<=10; i++)

{

System.out.print("Factorial of "+i+":");
ans=1;

j=i;

while(j>=1)

{

ans = ans * j;

if(j!=1)

System.out.print(j+"*");

else

System.out.print(j);

j--;

}

System.out.println("= "+ans);

}
}
}

3 Program to add two integers and two float numbers. When no arguments are supplied, give a default value to calculate the sum. Use function overloading.


import java.io.*;

 class Lab3
 
{

void add(int x, int y)

{

int sum = x + y;

System.out.println("Addition of two integer numbers "+x+" and "+y+" is "+sum);
}

void add(double x, double y)

{
double sum = x + y;

System.out.println("Addition of two floating point numbers "+x+" and"+y+" is "+sum);
}

public static void main(String []args) throws IOException
{

Lab3 ob = new Lab3();

ob.add(10,20);

ob.add(15.7, 18.6);

}
}



4 Program to perform mathematical operations. Create a class called AddSub with methods to add and subtract, Create another class called MulDiv that extends from AddSub class to use the member data of the super class. MulDiv should have methods to multiply and divide A main function should access the methods and perform the mathematical operations




import java.io.*;

 class AddSub
 
{
int add, sub;

public void add(int x, int y)
{

add = x + y;

System.out.println("Addition of 2 numbers ="+add);
}

public void sub(int x, int y)
{

sub = x - y;

System.out.println("Subtraction of 2 numbers ="+sub);
}

}
class MulDiv extends AddSub
{

int mul;

double div;

public void mul(int x, int y)
{

mul = x*y;

System.out.println("Multiplication of 2 numbers ="*Mul);
}

public void div(double x, double y)
{

if(y==0)

System.out.println("Division is not possible");

else

{
div = x / y;

System.out.println("Division of 2 numbers ="+div);
}

}
}
public class Lab4
{

public static void main(String []args) throws IOException
{

int a,b;

MulDiv ob = new MulDiv();

System.out.println("Enter two integer numbers");

DataInputStream ds = new DataInputStream(System.in);

a=Integer.parseInt(ds.readLine());

b=Integer.parseInt(ds.readLine());

ob.add(a,b);

ob.sub(a,b);

ob.mul(a,b);

ob.div(a,b);

}
}



5 Program with class variable that is available for all instances of a class. Use static variable declaration. Observe the changes that occur in the object's member variable values a.



import java.io.*;

 class Xyz
{

static int a;

public void accept() throws IOException

{
DataInputStream ds = new DataInputStream(System.in);

a= Integer.parseInt(ds.readLine());

}
public void display()

{
System.out.println("a="+a);

}
}
public class Lab5

{
public static void main(String []args) throws IOException

{
Xyz ob1 = new Xyz();

Xyz ob2 = new Xyz();

Xyz ob3 = new Xyz();

System.out.println("accept object1 'a' value:");

ob1.accept();

System.out.println("Object1 ");

ob1.display();

System.out.print("accept object2 'a' value:");

ob2.accept();

System.out.print("Object2 ");

ob2.display();

System.out.print("accept object3 'a' value:");

ob3.accept();

System.out.print("Object3 ");

ob3.display();

System.out.print("Object1 'a' value:");

ob1.display();

System.out.print("Object2 'a' value:");

ob2.display();

System.out.print("Object3 'a' value:");

ob3.display();
}
}

6  To find the area and circumference of the circle by accepting the radius from the user.



import java.io.*;

public class Radius

{
public static void main(String []args) throws IOException
{

int r;

float area = 0.0f, circum;

DataInputStream ds = new DataInputStream(System.in);

System.out.println("Enter the radius:");

r = Integer.parseInt(ds.readLine());

area = (3.142f * r * r);

circum = (2 * 3.142f * r * r);

System.out.println(" Area of the circle = "+area);

System.out.println("Circumference of the circle ="+circum);
}
}





7  To accept a number and find whether the number is Prime or not.


import java.io.*;

public class Prime

{
public static void main(String []args) throws IOException
{

int n,i,flag=0;

DataInputStream ds = new DataInputStream(System.in);

System.out.println("Enter a number:");

n = Integer.parseInt(ds.readLine());

for(i=2;i<n;i++)

{
if(n%i==0)

{
flag=1;

break;

}
}
if(flag==1)

System.out.println("Given number is not a prime number");

else

System.out.println("Given number is a prime number");

}
}

Part B

1  Program to catch Negative Array Size Exception. This exception is caused when the array is initialized to negative values.

public class Program11

{
public static void main(String []args)
{

try

{
int []a = new int[-5];

}
catch(NegativeArraySizeException e)
{

System.out.println(e);

System.out.println("Array size cannot be negative");
}

}
}

2  Program to handle Null Pointer Exception and use the "finally" method to display a message to the user.

class Program12

{
public static void main(String []args)throws IOException
{

try

{
String s =null;

int l =s.length();

System.out.println("Length of the string is"+1);

}
catch(NullPointerException e)

{
System.out.println(e);

}
finally

{
System.out.println("String value has been assigned null");
}

}
}



3 Program which create and displays a message on the window



import java.applet.Applet;

import java.awt.Graphics;

public class Program13 extends Applet
{

public void paint(Graphics g)
{

g.drawString("welcome to applet",200,200);
}

}


html
 
head
 
title First Applet /title

/head

body
 
applet code="Program13.class" width=400 height=400
/applet

/body

/html


4 Program to draw several shapes in the created window.


import java.applet.*;

import java.awt.*;

public class Program15 extends Applet

{
public void paint(Graphics g)

{
int x[]={100,150,200,350,175,280};

int y[]={100,180,300,450,350,200};

g.drawLine(350,50,150,150);

g.drawRect(450,100,550,150);

g.drawRoundRect(450,300,500,350,35,35);

g.drawOval(400,400,100,100);

g.drawOval(500,400,200,50);

g.drawArc(50,500,45,90,150,180);

g.drawPolygon(x,y,x.length);

}
}

html
 
head
 
title Shapes applet /title

/head

body
 
<applet code=Program15.class Width=800 height=800>
</applet>

/body

/html





5 Program to create an applet and draw grid lines.


import java.applet.*;

import java.awt.*;

public class Program16 extends Applet

{
public void paint(Graphics g)

{
int row, col, x=20, y=20;

for (row=1; row<=8;row++)

{
x=20;

for(col=1; col<=8; col++)
{

g.drawRect(x,y,20,20);

x=x+20;
}

y=y+20;
}

}
}


html
 
head
 
title Grid /title

/head

body
 
<applet code=Program16.class Width=800 height=800>
</applet>

/body

/html




6  Create a frame which displays your personal details with respect to a button click


import java.awt.*;

import java.awt.event.*;

class Program18 extends Frame implements ActionListener
{

Frame f;

Button b;

TextArea info;

public Program18()

{
//addMouseListener(this);

f = new Frame();

f.setSize(500,500);

f.setVisible(true);

f.setLayout(new FlowLayout());

b = new Button("CLICK FOR PERSONNEL DETAILS");

f.add(b);

info = new TextArea(20,25);

f.add(info);

b.addActionListener(this);

}
public void actionPerformed(ActionEvent e)

{
info.setText("Name: Vidya\n Course:BCA \n Contact No= 0123456789");

}
public static void main(String []args)
{

Program18 obj = new Program18();
}
}



7  Create simple applets which display the personal information of yours.



import java.applet.Applet;

import java.awt.Graphics;

public class Program14 extends Applet

{
public void paint(Graphics g)

{
g.drawString("Name :VIVIAN",100,100);

g.drawStrtng("Course :BCA",100,130);

}
}


html
 
head
 
title Personnel Information /title

/head

body
 
<applet code="Program14.class" width=400 height=400>
</applet>

/body

/html



8  Program to create a window when we press Morm the window displays Good Morning, A or a the window displays Good After Noon E or e the window displays Good Evening, N or n the window displays Good Night.

import java.awt.*;

import java.awt.event.*;

import java.awt.event.KeyEvent;

public class Program19 extends Frame implements KeyListener

{
Frame f;

char ch;

String str = "";

Label l;

public Program19()

{

f= new Frame();

f.setSize(500,500);

f.setVisible(true);

l= new Label();

l.setBounds(100, 100, 200, 40);

f.add(l);

f.addKeyListener(this);

}

public void keyTyped(KeyEvent e)

{

ch=e.getKeyChar();

switch(ch)

{

case 'M':

case 'm': l.setText("GOOD MORNING");break;

case 'A':

case 'a': l.setText("GOOD AFTERNOON");break;

case 'E':

case 'e': l.setText("GOOD EVENING");break;

case 'N':

case 'n': l.setText("GOOD NIGHT");

}

}

public void keyPressed(KeyEvent e)

{

}

public void keyReleased(KeyEvent e)

{

}

public static void main(String[]args)

{

new Program19();

}

}


9  Demonstrate the various mouse handling events using suitable example.




import java.awt.*;

import java.awt.event.*;

public class Program20a implements MouseListener,ActionListener
{

 static Frame f;
 
 static TextField text;
 
 public static void main(String[] args)
 
 {
 f=new Frame("Mouse Event");
 
 f.setSize(500,500);
 
f.setLayout(null);

 text=new TextField();
 
 text.setBounds(100,50,300,50);
 
 f.add(text);
 
 Button exit=new Button("Exit");
 
 exit.setBounds(220,235,60,30);
 
 f.add(exit);
 
 Program20a obj=new Program20a();
 
 f.addMouseListener(obj);
 
 exit.addActionListener(obj);
 
 f.setVisible(true);
 
 }
@Override

 public void actionPerformed(ActionEvent e)
 
 {
 f.dispose();
 
 }
@Override

 public void mouseEntered(MouseEvent e)
 
 {
 text.setText("");
 
 text.setText("Mouse Entered the frame ");
 
 }
@Override

 public void mouseExited(MouseEvent e)
 
 {
 text.setText("");
 
text.setText("Mouse Exited the frame"); 

 }
@Override

 public void mouseReleased(MouseEvent e)
 {
 
 text.setText("");
 
 String button="Right";
 
 if(e.getButton()==MouseEvent.BUTTON1)
 
 button="Left";
 
 text.setText(button+" Button Released");
 }
 
 @Override
 
 public void mousePressed(MouseEvent e)
 {
 
 text.setText("");
 
 String button="Right";
 
 if(e.getButton()==MouseEvent.BUTTON1)
 
 button="Left";
 
 text.setText(button+" Button Pressed");
 }
@Override

 public void mouseClicked(MouseEvent e)
 {
 
 text.setText("");
 
 String button="Right";
 
 if(e.getButton()==MouseEvent.BUTTON1)
 
 button="Left";
 
text.setText(button+" Button Clicked");
 }
 
}























