# Ex.No:2
# Ex.Name:Write A CPP Program to create class RectangleBox and calculate the volume of the rectangleBoxe use of static member variable in the class RectangleBox.
## Date:
## Aim:
To write a C++ program to overload the + operator for adding two objects of a Box class. Each object contains height, length, and breadth. After addition, compute the volume of the resultant object.

## Algorithm:
1. Start the program.
2. Define a class Box with three data members: height, length, and breadth.
3. Define a constructor to initialize the box dimensions.
4. Define a method volume() to calculate and return the volume of the box.
5. Overload the + operator to add the dimensions of two Box objects and return a new Box object.
6. In main(), create two objects of the Box class and display their dimensions and volumes.
7. Use the overloaded + operator to create a third object whose dimensions are the sum of the first two objects.
8. Display the dimensions and volume of the third object.
9. End the program.




## Program:
```
#include <iostream>
using namespace std ;

class Box {
   public:
      double getVolume(void) {
         return length * breadth * height;
      }
      void setLength( double len ) {
         length = len;
      }
      void setBreadth( double bre ) {
         breadth = bre;
      }
      void setHeight( double hei ) {
         height = hei;
      }
      Box operator+(const Box& b) {
         Box box;
         box.length = this->length + b.length;
         box.breadth = this->breadth + b.breadth;
         box.height = this->height + b.height;
         return box;
      }
      
   private:
      double length;      
      double breadth;     
      double height;      
};
int main() {
   Box Box1;             
   Box Box2;       
   Box Box3;           
   double volume = 0.0;
   double a,b,c;
   cin>>a>>b>>c;
   Box1.setLength(a); 
   Box1.setBreadth(b); 
   Box1.setHeight(c);
   cin>>a>>b>>c;
   Box2.setLength(a); 
   Box2.setBreadth(b); 
   Box2.setHeight(c);
   volume=Box1.getVolume();
   cout<<"Volume of Box1 : "<<volume<<endl;
   volume = Box2.getVolume();
   cout<<"Volume of Box2 : "<<volume<<endl;
   Box3=Box1+Box2;
   volume=Box3.getVolume();
   cout<<"Volume of Box3 : "<<volume<<endl;
   return 0;
}
```



## Output:
<img width="528" height="290" alt="485442713-9ddbb66e-320d-4dd5-b52d-0cf8f8f70a67" src="https://github.com/user-attachments/assets/18459c63-0212-497a-8b5d-afa31f7191b3" />



## Result:
The program successfully overloads the + operator to add two Box objects by summing their dimensions and then calculates the volume of the resultant box.
