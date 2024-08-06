\\1a\\\\\\\\\\\\\\\\\\\\\
1a
package p1;
import java.util.Scanner;
public class lab1 {
public static void main(String[] args) {
int a,b;
String ch;
Scanner sc = new Scanner(System.in);
System.out.println("Enter the operand 1:");
a=sc.nextInt();
System.out.println("Enter the operator:");
ch=sc.next();
System.out.println("Enter the operand 2:");
b=sc.nextInt();
switch(ch) {
case"+":
System.out.println("the value is:");
System.out.println(a+b);
break;
case"-":
System.out.println("the value is:");
System.out.println(a-b);
break;
case"*":
System.out.println("the value is:");
System.out.println(a*b);
break;
case"/":
System.out.println("the value is:");
System.out.println((float)a/(float)b);
break;
case"%":
System.out.println(a%b);
break;
default:
System.out.println("Invalid Operator!!! Enter the valid operator");
}
}
}
\\\\\1b\\\\\\\\\\\\\\\\\\\\
1. B) Write a Java program to generate the first 'n' terms of the Fibonacci series
package p1;
import java.util.Scanner;
public class Lab_Program_1b {
public static void main(String[] args)
{
int n, i, first, second, next;
System.out.println("Enter the value of n");
Scanner sc = new Scanner(System.in);
n=sc.nextInt();
first=0;
second=1;
System.out.println("Fibonacci series are:\n");
System.out.print(first+"\t"+second);
for(i=2;i<=n-1;i++)
{
next=first+second;
System.out.print("\t"+next);
first=second;
second=next;
}
}}

2a
package p1;
class phone
{
void dial() {
System.out.println("Calling friend using this number through a regular phone");
}
}
class camera_phone extends phone {
void dial(String n) {
System.out.println("calling "+n+"using camera phone");
}
void take_photo() {
System.out.println("Take photo using camera phone");
}
}
class smart_phone extends camera_phone{
void dial(String n , boolean b) {
if(b) {
}
else {
}
}
System.out.println("calling "+n+"through video call");
System.out.println("calling "+n+"through normal voice call");
void acces_internet() {
System.out.println("Accessing internet for WWW");
} }
public class Lab_Program2a {
public static void main(String[] args) {
phone p=new phone();
p.dial();
camera_phone c=new camera_phone();
c.dial();
c.dial("Priya ");
c.take_photo();
smart_phone s=new smart_phone();
s.dial("Priya ",true);
s .acces_internet();
}
}

\\\\\2b\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
package p1;
import java.math.*;
class Shape_A_C{
Shape_A_C(int r){
System.out.println("A circle is created");
System.out.println("Area of circle which was created is
"+(Math.PI*r*r)+" cm2");
}
Shape_A_C(int l,int b){
System.out.println("A rectangle is created");
System.out.println("Area of rectangle which was created is
"+(l*b)+"cm2");
}
}
public class Lab_Program2b {
public static void main(String[] args) {
new Shape_A_C(4);
new Shape_A_C(3,4);
}
}

\\\\3a\\\\\\\\\\\\\\\\\\\\\
package p1;
class vehicles
{
void start()
{
System.out.println("vehicle started");
}
void stop() {
System.out.println("vehicle stopped");
}
}
class car extends vehicles
{
void start()
{
System.out.println("car started");
}
void stop() {
System.out.println("carstopped");
}
void accelerate() {
System.out.println("accelerating in a car");
}
}
class sports_car extends vehicles{
void start() {
System.out.println("sports car started");
}
void stop() {
System.out.println("sports car stopped");
}
void turbo() {
System.out.println("Sports turbo boosting in my sports car");
}
}
class truck extends vehicles{
void start() {
System.out.println("truck started");
}
void stop() {
System.out.println("truck stopped");
}
void load_cargo() {
System.out.println("load cargo into the truck");
}
}
public class Lab_Program3a{
public static void main(String[] args) {
car c1=new car();
c1.start();
c1.accelerate();
c1.stop();
sports_car s1=new sports_car();
s1.start();
s1.turbo();
s1.stop();
truck t1=new truck();
t1.start();
t1.load_cargo();
t1.stop();
}
}

\\\\\3b\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
package p1;
interface power_management{
void poweron();
void poweroff();
boolean ispoweron();
}
class electronic_devices implements power_management{
boolean state=false;
public void poweron() {
state=true;
System.out.println("electronic device is turnes on");
}
public void poweroff() {
state=false;
System.out.println("electronic device is turnes off");
}
public boolean ispoweron(){
return state;
}
}
class smart_phone1 extends electronic_devices{
public void poweron() {
state=true;
System.out.println("smart phone is turned on");
}
public void poweroff() {
state=false;
System.out.println("smart phone is turned off");
}
void
dial() {
if(ispoweron())
System.out.println("call my friend using smart phone");
else
System.out.println("hey idiot,first turn on the phone");
}
}
class laptop extends electronic_devices{
public void poweron() {
state=true;
System.out.println("laptop is turnes on");
}
public void poweroff() {
state=false;
System.out.println("laptop is turned off");
}
void access_internet() {
if(ispoweron())
System.out.println("accessing internet using laptop");
else
System.out.println("please turn on laptop");
}
}
class tablet extends electronic_devices{
public void poweron() {
state=true;
System.out.println("tablet is turned on");
}
public void poweroff() {
state=false;
System.out.println("tablet off");
}
void takephoto() {
if(ispoweron())
System.out.println("taking photo using tablet");
else
System.out.println("please turn on tablet");
}
}
public class Lab_Program3b {
public static void main(String[] args) {
smart_phone1 oneplus=new smart_phone1();
oneplus.poweron();
oneplus.dial();
oneplus.poweroff();
oneplus.dial();
System.out.println();
tablet ipad=new tablet();
ipad.poweron();
ipad.takephoto();
ipad.poweroff();
ipad.takephoto();
}
}

\\\\4a\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
package library;
public class Book {
private String title=null;
public Book(String title)
{
this.title=title;
System.out.println("The book titled "+this.title+" is added to the library");
}
public String getTitle()
{
return title;
}
}
/////step2

package patron;
import library.Book;
public class Patron
{
public String name=null;
Patron(String name)
{
this.name=name;
System.out.println("New patron "+this.name+" is added to the database");
}
void borrow_books(Book b)
{
System.out.println(this.name+" borrowed "+b.getTitle());
}
}
//////step3
package patron;
import library.Book;
public class Demo_Library_Management_System {
public static void main(String[] args) {
Book b1=new Book("AR sir's notes");
Book b2=new Book("Little champs");
Patron p1=new Patron("Chandana");
Patron p2=new Patron("Deeksha");
p1.borrow_books(b1);
p1.borrow_books(b2);
}
}

\\\\4b\\\\\\\\\\\\\\\\\\\\\\\\\\\\
package p1;
import java.util.Scanner;
import java.util.InputMismatchException;
public class Lab_Program4b {
public static void main(String[] args) {
Scanner s=new Scanner(System.in);
int c=0,a=0,b=0;
try {
while(true) {
try {
}
System.out.println("Enter the numerator:");
a=s.nextInt();
break;
catch(InputMismatchException f) {
System.out.println("Give only integer input for numerator");
s.nextLine();
}
}
while(true){
try {
}
System.out.println("Enter the denominator:");
b=s.nextInt();
c=a/b;
break;
catch(InputMismatchException f) {
System.out.println("Give only integer input for denominator");
s.nextLine();
}
catch(ArithmeticException f) {
System.out.println("The denominator value should be greater than zero");
s.nextLine();
}
}
}
finally{
s.close();
}
System.out.println("c="+c);
}
}

\5a\\\\\\\\\\\\\\\\\\\\\\\\\\\\
package p1;
import java.util.Random;
class RandomNumbers implements Runnable{
public void run() {
for(int i=0;i<10;i++) {
Random rn=new Random();
int num=rn.nextInt(10);
System.out.println(num);
new Sq_Of_Random(num);
new Cube_Of_Random(num);
try {
Thread.sleep(1000);
}catch(InterruptedException e) {
e.printStackTrace();
}
}
}
}
class Sq_Of_Random implements Runnable{
int num;
Sq_Of_Random(int num){
this.num=num;
new Thread(this).start();
}
public void run() {
num=num*num;
System.out.println(num);
}
}
class Cube_Of_Random implements Runnable{
int num;
Cube_Of_Random(int num){
this.num=num;
new Thread(this).start();
}
public void run() {
num=num*num*num;
System.out.println(num);
}
}
public class Lab_Program_5a {
public static void main(String[] args) {
Runnable r1=new RandomNumbers();
new Thread(r1).start();
}
}

\\\\\5b\\\\\\\\\\\\\\\\\\\\\\\\
package p1;
import java.util.Scanner;
public class Lab_Program_5b {
public static void main(String[] args) {
Scanner Scn = new Scanner(System.in);
System.out.println("Enter the first string :");
String S1 = Scn.next();
System.out.println("Enter the second string : ");
String S2 = Scn.next();
String S3 = new String(S1.concat(S2));
System.out.println("The concatenation string is :" + S3);
System.out.println("Extract portion from concatenated string is :" + S3.substring(3));
if (S1.equals(S2)) {
System.out.println("Strings you have entered are equal ");
} else {
System.out.println("Strings you have entered are not equal");
}
Scn.close();
}
}
