//# intech-additive-solutions

A)-



import java.util.*;


public class Main{
public static void main(String args[]){ Scanner sc = new Scanner(System.in); String myString = sc.next();

int counter = 0; int num = 0; char c = 0;

for(int i=0;i<myString.length();i++){


if(i%2 != 0){
num = Integer.parseInt(Character.toString(myString.charAt(i)));


}else if(i%2 == 0){
c = myString.charAt(i);

}
counter++;


if(counter == 2){
for(int j=0;j<num;j++){ System.out.print(c);

}
counter = 0;
}



}
}
}



B)-
/** This is the ListNode class definition


class ListNode {
int data;
ListNode next;


ListNode(int data) {
this.data = data; this.next = null;
}
}
**/



class Solution {
ListNode kthElement (ListNode head, int k) { int index = 0;
ListNode currentNode = head;

while(currentNode != null) { index++;
if(index == k) {
break;

}
currentNode = currentNode.next;
}

return currentNode;
}
}


C)-
Stack



Fundamentally whenever you need to put a reverse gear & get the elements in
constant time,use a Stack. Stack follows LIFO it’s just a way of arranging data.


Application:


1)Achieving the undo operation in notepads.
2)Browser back button uses a Stack.
Because they help manage your data in more a particular way than arrays and lists.
Stack is last in, first out (LIFO)
Arrays and lists are random access. They are very flexible and also easily corruptible. IF you want to manage your data as FIFO or LIFO it's best to use those, already implemented, collections.

D)-
public static int trapping_rain_water(int[] A, int N)
{

int res = 0;
for(int i = 0; i < N ; i++)
{

int left_max= arr[i]; for(int j = i - 1; j >= 0; j--)
{

left_max = Math.max(left_max, A[j]);
}

int right_max = A[i]; for(int j = i + 1; j < n; j++)
{

right_max = Math.max(right_max, A[j]);
}

res += Math.min(left_max, right_max) - A[i];
}

return res;
}



E)-
import java.util.Vector; import java.util.*;
class Main
{


static int deno[] = {1, 2, 5, 8, 10}; static int n = deno.length;

static void findMin(int V)
{


Vector<Integer> ans = new Vector<>();


for (int i = n - 1; i >= 0; i--)
{


while (V >= deno[i])
{

V -= deno[i]; ans.add(deno[i]);
}
}





for (int i = 0; i < ans.size(); i++)
{

System.out.print(ans.elementAt(i)+	" " );
}
}

public static void main(String[] args)
{

Scanner s=new Scanner(System.in); int n = s.nextInt();
findMin(n);
}
}

                                            Dynamic Programming	
1.Dynamic Programming is used to obtain the optimal solution.
2.In Dynamic Programming, we choose at each step, but the choice may depend on the solution to sub- problems.
3.Less efficient as compared to a greedy approach
4.Example: 0/1 Knapsack
5.It is guaranteed that Dynamic Programming will generate an optimal solution using Principle of Optimality.
                                             Greedy Method
1.Greedy Method is also used to get the optimal solution.
2.In a greedy Algorithm, we make whatever choice seems best at the moment and then solve the sub- problems arising after the choice is made.
3.More efficient as compared to a greedy approach
4.Example: Fractional Knapsack
5.In Greedy Method, there is no such guarantee of getting Optimal Solution


import java.util.*;


import java.math.*;



class Main{


static int maxnumber(int n, int k)
{

for (int j = 0; j < k; j++) { int ans = 0;
int i = 1;
while (n / i > 0) {
int temp = (n / (i * 10))* i + (n % i); i *= 10;
ans = Math.max(ans, temp);

}
n = ans;
}

return n;
}

public static void main(String[] args)
{

int n = 19374; int k = 1;
System.out.println(maxnumber(n,k));



}
}


F)-

Scalar Product/Dot Product of Vectors
The resultant of scalar product/dot product of two vectors is always a scalar quantity. Consider two vectors a and b. The scalar product is calculated as the product of magnitudes of a, b, and cosine of the angle between these vectors.
Scalar product = |a||b| cos α

Cross Product/Vector Product of Vectors
Readers are already familiar with a three-dimensional right-handed rectangular coordinate system. In this system, a counterclockwise rotation of the x-axis into the positive y-axis indicates that a right-handed (standard) screw would advance in the direction of the positive z-axis.


G)- Bank account:-

class Bank_Account:
def     init   (self):
self.balance=0
print("Hello!!! Welcome to the Deposit & Withdrawal Machine")


def deposit(self):
amount=float(input("Enter amount to be Deposited: ")) self.balance += amount
print("\n Amount Deposited:",amount)


def withdraw(self):
amount = float(input("Enter amount to be Withdrawn: ")) if self.balance>=amount:
self.balance-=amount
print("\n You Withdrew:", amount)

else:
print("\n Insufficient balance ")


def display(self):

print("\n Net Available Balance=",self.balance) s = Bank_Account()
s.deposit() s.withdraw() s.display()

H)-

There could be some general cases which may result in such behavior


Random Variable : The application may be using some random variable, like random number generator or a specific time of the day or a user input etc which may be causing this.

Uninitialized Variable : May be there is some uninitialized variable, which takes an arbitrary value each time and those values are causing such drastic behavior.

Memory Leak : The program may have run out of memory, maybe heap overflow or something.

External Dependencies : The program may depend on some other application which is causing this.

Other process on machine : Maybe there are some other processes, running on machine causing it.



Computer architecture can be defined as a set of rules and methods that describe the functionality, management and implementation of computers. To be precise, it is nothing but rules by which a system performs and operates.


Sub-divisions

Computer Architecture can be divided into mainly three categories, which are as follows −


Instruction set Architecture or ISA − Whenever an instruction is given to processor, its role is to read and act accordingly. It allocates memory to instructions and also acts upon memory address mode (Direct Addressing mode or Indirect Addressing mode).


Micro Architecture − It describes how a particular processor will handle and implement instructions from ISA.


System design − It includes the other entire hardware component within the system such as virtualization, multiprocessing.


Role of computer Architecture

The main role of Computer Architecture is to balance the performance, efficiency, cost and reliability of a computer system.


For Example − Instruction set architecture (ISA) acts as a bridge between computer's software and hardware. It works as a programmer's view of a machine.


Computers can only understand binary language (i.e., 0, 1) and users understand high level language (i.e., if else, while, conditions, etc). So to communicate between user and computer, Instruction set Architecture plays a major role here, translating high level language to binary language.


Structure

Let us see the example structure of Computer Architecture as given below.


Generally, computer architecture consists of the following −


Processor


Memory


Peripherals


All the above parts are connected with the help of system bus, which consists of address bus, data bus and control bus.
