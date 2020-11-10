# Bug 1

1. **The incorrect original code or code snippit that you wrote:**

#include <iostream>
using namespace std;
class Student{

        string name;
        string number;
        int age;
        public:
        Student(string k,string nb,int a){
                name=k;
                number=nb;
                age=a;
        }
        
         string getNumber() {
                return number;
        }
         int getAge() {
                return age;
        }
        string getName() {
                return name;
        }
         void setName(string aName) {
                name = aName;
        }
         void setNumber(string aNumber) {
                number = aNumber;
        }
         void setAge(int aAge) {
                age = aAge;
        }
        
};
class KpuStudent:public Student{
        string major;
        string campus;
        int year;
        public:
        KpuStudent(string name,string number,int age,string mr,string cs,int y):Student(name,number,age){
                major= mr;
                campus=cs;
                year=y;
        }
         string getMajor() {
                return major;
        }
         string getCampus() {
                return campus;
        }
         int getYear() {
                return year;
        }
         void setMajor(string aMajor) {
                major = aMajor;
        }
         void setCampus(string aCampus) {
                campus = aCampus;
        }
         void setYear(int aYear) {
                year = aYear;
        }
         display(){
                cout<<"Name: "<<getName()<<endl;
                cout<<"Number: "<<getNumber()<<endl;
                
                cout<<"Major: "<<getMajor()<<endl;
                cout<<"Campus: "<<getCampus()<<endl;
                cout<<"Year: "<<getYear()<<endl;
                cout<<"Age: "<<getAge()<<endl;
                
        }
};
int main(){
        KpuStudent kp ("Harno","100394840","CIS","Rn",1,20);
        kp.display();
}

2. **What bug does the original code have?**
 display(){
  

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
C++ forbids declaration of 'display' with no type [-fpermissive]

4. **How to correct the bug?**
  void display(){

5. **The corresponding bug-free code or code snippet is:**

```
#include <iostream>
using namespace std;
class Student{

        string name;
        string number;
        int age;
        public:
        Student(string k,string nb,int a){
                name=k;
                number=nb;
                age=a;
        }
        
         string getNumber() {
                return number;
        }
         int getAge() {
                return age;
        }
        string getName() {
                return name;
        }
         void setName(string aName) {
                name = aName;
        }
         void setNumber(string aNumber) {
                number = aNumber;
        }
         void setAge(int aAge) {
                age = aAge;
        }
        
};
class KpuStudent:public Student{
        string major;
        string campus;
        int year;
        public:
        KpuStudent(string name,string number,int age,string mr,string cs,int y):Student(name,number,age){
                major= mr;
                campus=cs;
                year=y;
        }
         string getMajor() {
                return major;
        }
         string getCampus() {
                return campus;
        }
         int getYear() {
                return year;
        }
         void setMajor(string aMajor) {
                major = aMajor;
        }
         void setCampus(string aCampus) {
                campus = aCampus;
        }
         void setYear(int aYear) {
                year = aYear;
        }
        void display(){
                cout<<"Name: "<<getName()<<endl;
                cout<<"Number: "<<getNumber()<<endl;
                
                cout<<"Major: "<<getMajor()<<endl;
                cout<<"Campus: "<<getCampus()<<endl;
                cout<<"Year: "<<getYear()<<endl;
                cout<<"Age: "<<getAge()<<endl;
                
        }
};
int main(){
        KpuStudent kp ("Harno","100394840","CIS","Rn",1,20);
        kp.display();
}


```


---

# Bug 2

1. **The incorrect original code or code snippit that you wrote:**

```
#include <iostream>
using namespace std;
class Student{

        string name;
        string number;
        int age;
        public:
        Student(string k,string nb,int a){
                name=k;
                number=nb;
                age=a;
        }
        
         string getNumber() {
                return number;
        }
         int getAge() {
                return age;
        }
        string getName() {
                return name;
        }
         void setName(string aName) {
                name = aName;
        }
         void setNumber(string aNumber) {
                number = aNumber;
        }
         void setAge(int aAge) {
                age = aAge;
        }
        
};
class KpuStudent:public Student{
        string major;
        string campus;
        int year;
        public:
        KpuStudent(string name,string number,int age,string mr,string cs,int y):Student(name,number,age){
                major= mr;
                campus=cs;
                year=y;
        }
         string getMajor() {
                return major;
        }
         string getCampus() {
                return campus;
        }
         int getYear() {
                return year;
        }
         void setMajor(string aMajor) {
                major = aMajor;
        }
         void setCampus(string aCampus) {
                campus = aCampus;
        }
         void setYear(int aYear) {
                year = aYear;
        }
        void display(){
                cout<<"Name: "<<getName()<<endl;
                cout<<"Number: "<<getNumber()<<endl;
                
                cout>>"Major: "<<getMajor()<<endl;
                cout<<"Campus: "<<getCampus()<<endl;
                cout<<"Year: "<<getYear()<<endl;
                cout<<"Age: "<<getAge()<<endl;
                
        }
};
int main(){
        KpuStudent kp ("Harno","100394840","CIS","Rn",1,20);
        kp.display();
}


```

2. **What bug does the original code have?**
cout>>"Major: "<<getMajor()<<endl;

  

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
misunderstanding regarding the characters


4. **How to correct the bug?**

                cout<<"Major: "<<getMajor()<<endl;
5. **The corresponding bug-free code or code snippet is:**

```
#include <iostream>
using namespace std;
class Student{

        string name;
        string number;
        int age;
        public:
        Student(string k,string nb,int a){
                name=k;
                number=nb;
                age=a;
        }
        
         string getNumber() {
                return number;
        }
         int getAge() {
                return age;
        }
        string getName() {
                return name;
        }
         void setName(string aName) {
                name = aName;
        }
         void setNumber(string aNumber) {
                number = aNumber;
        }
         void setAge(int aAge) {
                age = aAge;
        }
        
};
class KpuStudent:public Student{
        string major;
        string campus;
        int year;
        public:
        KpuStudent(string name,string number,int age,string mr,string cs,int y):Student(name,number,age){
                major= mr;
                campus=cs;
                year=y;
        }
         string getMajor() {
                return major;
        }
         string getCampus() {
                return campus;
        }
         int getYear() {
                return year;
        }
         void setMajor(string aMajor) {
                major = aMajor;
        }
         void setCampus(string aCampus) {
                campus = aCampus;
        }
         void setYear(int aYear) {
                year = aYear;
        }
        void display(){
                cout<<"Name: "<<getName()<<endl;
                cout<<"Number: "<<getNumber()<<endl;
                
                cout<<"Major: "<<getMajor()<<endl;
                cout<<"Campus: "<<getCampus()<<endl;
                cout<<"Year: "<<getYear()<<endl;
                cout<<"Age: "<<getAge()<<endl;
                
        }
};
int main(){
        KpuStudent kp ("Harno","100394840","CIS","Rn",1,20);
        kp.display();
}


```

6. **What is the take-away message from this bug?**
c++ is character specific

---

# Bug 3

1. **The incorrect original code or code snippit that you wrote:**

```
#include <iostream>
using namespace std;
class Student{

        string name;
        string number;
        int age;
        public:
        Student(string k,string nb,int a){
                name=k;
                number=nb;
                age=a;
        }
        
         getNumber() {
                return number;
        }
         int getAge() {
                return age;
        }
        string getName() {
                return name;
        }
         void setName(string aName) {
                name = aName;
        }
         void setNumber(string aNumber) {
                number = aNumber;
        }
         void setAge(int aAge) {
                age = aAge;
        }
        
};
class KpuStudent:public Student{
        string major;
        string campus;
        int year;
        public:
        KpuStudent(string name,string number,int age,string mr,string cs,int y):Student(name,number,age){
                major= mr;
                campus=cs;
                year=y;
        }
         string getMajor() {
                return major;
        }
         string getCampus() {
                return campus;
        }
         int getYear() {
                return year;
        }
         void setMajor(string aMajor) {
                major = aMajor;
        }
         void setCampus(string aCampus) {
                campus = aCampus;
        }
         void setYear(int aYear) {
                year = aYear;
        }
        void display(){
                cout<<"Name: "<<getName()<<endl;
                cout<<"Number: "<<getNumber()<<endl;
                
                cout<<"Major: "<<getMajor()<<endl;
                cout<<"Campus: "<<getCampus()<<endl;
                cout<<"Year: "<<getYear()<<endl;
                cout<<"Age: "<<getAge()<<endl;
                
        }
};
int main(){
        KpuStudent kp ("Harno","100394840","CIS","Rn",1,20);
        kp.display();
}


```

2. **What bug does the original code have?**

  getNumber()

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
misunderstandings of the constructors

4. **How to correct the bug?**
 string getNumber()

5. **The corresponding bug-free code or code snippet is:**

```
#include <iostream>
using namespace std;
class Student{

        string name;
        string number;
        int age;
        public:
        Student(string k,string nb,int a){
                name=k;
                number=nb;
                age=a;
        }
        
         string getNumber() {
                return number;
        }
         int getAge() {
                return age;
        }
        string getName() {
                return name;
        }
         void setName(string aName) {
                name = aName;
        }
         void setNumber(string aNumber) {
                number = aNumber;
        }
         void setAge(int aAge) {
                age = aAge;
        }
        
};
class KpuStudent:public Student{
        string major;
        string campus;
        int year;
        public:
        KpuStudent(string name,string number,int age,string mr,string cs,int y):Student(name,number,age){
                major= mr;
                campus=cs;
                year=y;
        }
         string getMajor() {
                return major;
        }
         string getCampus() {
                return campus;
        }
         int getYear() {
                return year;
        }
         void setMajor(string aMajor) {
                major = aMajor;
        }
         void setCampus(string aCampus) {
                campus = aCampus;
        }
         void setYear(int aYear) {
                year = aYear;
        }
        void display(){
                cout<<"Name: "<<getName()<<endl;
                cout<<"Number: "<<getNumber()<<endl;
                
                cout<<"Major: "<<getMajor()<<endl;
                cout<<"Campus: "<<getCampus()<<endl;
                cout<<"Year: "<<getYear()<<endl;
                cout<<"Age: "<<getAge()<<endl;
                
        }
};
int main(){
        KpuStudent kp ("Harno","100394840","CIS","Rn",1,20);
        kp.display();
}


```



