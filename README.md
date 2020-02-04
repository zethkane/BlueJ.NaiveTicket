# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
0
### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?
	when the ticket is printed the balance keeps your total keeps rising.
	* What happens if you insert too much money into the machine – do you receive any refund? No refund is issued.
	* What happens if you do not insert enough and then try to print a ticket? The string still says "Ticket price: 15 cents. Your total is 10." Just like it would if I put enough into the machine.

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different? The ticket looks the same just displays the new price.

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
public class Student
public class LabClass
### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class? Yes it does, class public TicketMachine won't run, saying < identifier > expected.

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
	* What error message do you get when you now press the compile button?
	* Do you think this message clearly explains what is wrong?

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class. It is possible to leave out public and the file still compiles.

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.
constructor:
public TicketMachine(Integer ticketCost)
        price = ticketCost;
        balance = 0;
        total = 0;
        ticketNumber = 0;
Fields:
private Integer price;
private Integer balance;
private Integer total;
private Integer ticketNumber;

Methods:
public Integer getPrice()
        {
            return price;
public Integer getTicketNumber()
		    {
		        return ticketNumber;
public Integer getBalance()
				{
						return balance;
public Integer insertMoney(Integer amount)
				{
						balance = balance + amount;
						return balance;
public Integer calculateTotal(){
						total = balance + total;
		        return total;				
public Integer incrementTicketNumber(){
		        ticketNumber++;
		        return ticketNumber;
public String printTicket()
						    {
						        //Increment the number of tickets printed
						        incrementTicketNumber();
						        // Update the total collected with the balance.
						        total = total + balance;
						        // Clear the balance.
						        balance = 0;
### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
It holds values for the fields used in the code.
### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count; // This field is a int.
private Student representative; // This field is a Student.
private Server host; // This field is a Server.
```

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive; // This field is a boolean.
private Person tutor; // This field is a Person.
private Game game; // This field is a Game.
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
Yes the order does matter since "int" is making price a field if "int" was before private, it would make private a field.

* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
Yes the diagram does not change after trying different orderings, giving the hint that other orderings are not possible.
	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
Yes it is, using a semicolon tells the compiler that it's the end of a declaration.
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.
public int status;
### Exercise 2.16
* To what class does the following constructor belong?
```
public Student(String name)
```
It belongs to the Student class.
### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)
```
It has 2 parameters and their types are String and double.
### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
Some could be String, float and int.
* Can you assume anything about the names of its fields?
I can assume that every Book has a Title, price, and Author.
READ upto and INCLUDING section 2.15 of this chapter.
