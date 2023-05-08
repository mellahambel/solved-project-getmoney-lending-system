Download Link: https://assignmentchef.com/product/solved-project-getmoney-lending-system
<br>
Your project is to build a prototype for GetMoney Inc. that manages customer accounts that have borrowed money. GetMoney allows customers to both deposit or payback money that was borrowed and withdraw or borrow funds from their GetMoney account. Customers are only allowed to make up to 5 transactions each day (payback or borrow). Your application will track each customer’s account balance which can be either positive or negative. When a customer wants to borrow money they will enter the amount needed and it will be dispensed to them after verifying their security data. After confirming the amount borrowed, their account balance will be updated reflecting the amount borrowed. When a customer is making a payment to payback money borrowed a 10% fee will be subtracted from the payment and then the customer’s account will be updated. Your application will allow a customer the ability to view their transaction made during a single-usage session using the application. Customers must be able to view their balance, borrow and/or payback money, modify their customer information, display 5 transaction history, and logout. To ensure security you must customer accounts are only accessed if the correct security information is entered. GetMoney will start each day with $25,000.00. See below for more requirements:

Design a Lending application prototype. Your application shall take advantage of the C# programming language to provide a way to rapidly develop a working prototype. The application must have the following requirements:

NOTE: Test data will follow at a later date listing objects and data that must be in your final deliverable in order to expedite testing.

Create the following 2 classes:

<ul>

 <li>  A Main menu class where a user will access the functions of your program.</li>

 <li>  A Class that manages customer Accounts.</li>

</ul>

Each class must contain the following data and perform these actions:  The Menu class will contain the following data:

o Track login status to determine when a user is logged in (user was authenticated) and logged out. Transaction menus shall not be accessible until a customer is logged in.

o Track the amount of money available at GetMoney. Assume they start each day with a cash balance of $25,000.00.

 The Menu class will perform the following (use other classes to break up this work): o Upon starting the application a user will be prompted to login. The first action is to

authenticate the user by validating an account exists for the entered username. Once the username has been matched to an account, validate the entered pin (see Account class). You must validate both before logging a customer into the system.

o After authentication, display a welcome message to the customer logged in using their name stored in their customer account and display a menu offering options:

 View account balance  Borrow or Payback  Modify customer information  View current transactions  Logout

o View account balance will display the amount of money in the logged-in user’s account. Positive values mean they do not owe any money and actually have a credit. Negative values indicate the customer has borrowed money and must pay back the borrowed money at some point in time.

o Update GetMoney’s available cash based on how much money is borrowed or paid back while transaction occur. GetMoney’s available cash is not allowed to go below $0 o Borrow or Payback will allow customers to enter a dollar amount to borrow or payback.

Any payback dollar amount entered will have a 10% lending fee deducted before updating a customer’s account balance. Borrowed amounts do not involve any fees. Example: GetMoney currently has $5000 cash on-hand and a customer’s account balance is -$100 so they owe money. If the customer makes a payment of $100 a 10% fee is charged $10 so only $90 dollars is applied to the owed amount making the customer’s new balance -$10. Since $100 was paid we also update GetMoney’s cash available to $5100.

o Modify account information upon user request. This allows the user the ability to modify their account information using a sub-menu:

 Name  Address  Username  Pin

o Display transaction history of the current session (5 possible transactions) when selected. When displaying each transaction show only positive numbers with the text “Payback” or “Borrowed” next to each value indicating which action was performed. Make a decision on each value where positive values are paybacks and negatives are borrowed when displaying the history.

o Upon a user logout return back to the beginning asking for a username and pin. o Implement a counter to track the number of transactions. Increment for each and every

deposit or withdrawal made. A customer is allowed to make up to 5 transactions on a

single login. Reset counter for each login. o Track a history of the 5 possible transactions. This will be an array of dollar amounts

where a negative amount is a withdrawal and a positive number is a deposit. Clear the

history each time a customer logs in and reset the transaction counter. o Update history to reflect any transaction made when a user is logged in. Keep track of each transaction value made as described above in the transaction data section. After

each transaction, increment the transaction counter.  Account objects will contain data:

o name – first and last name of the customer. o address – number, direction, street/ave name, state, and zip o username – must be at least 4 characters of mixed letters &amp; numbers. o pin – must be a 4 digit number. o balance – dollar amount in customer’s account (updated per withdrawals/deposits).

Format with a dollar sign and two decimal places any time it is displayed. o creditLimit – total amount of money a customer is allowed to borrow.

 Account objects will perform the following: o Validate the entered PIN matches the account pin. o Perform transactions and update account balance based on the borrowed/payback

amount. o Get balance when the balance is requested and return for display purposes.

 GetMoney is not able to dispense more cash than is available. Inform the customer when they are out of cash (Insufficient funds) in the event GetMoney is out of money.

<ul>

 <li>  When GetMoney’s available cash is low and a customer requests more money than available, notify the customer of how much money can be borrowed ($$$$ remains)</li>

 <li>  Customers are not allowed to borrow more than their credit limit for their account. In the event a customer attempts to borrow a combined total (amount currently owed + borrowed amount) of more than the remaining credit available, display an informative message stating how much money is remaining in their credit limit.</li>

 <li>  The application only closes upon the administrative login. The admin will not have an account (this means you cannot create an account object for admin). The admin username and password will be in Account class as class variables. Admin username is r00t and pin is 0000.</li>

 <li>  Validate entered data and ensure the program does not crash due to bad data entries. Implement exception handling when needed.
 General Requirements</li>

</ul>

 The project needs to be implemented as a C# Console Application in Visual Studio 2015.

o Do not submit Visual Studio 2017 files.  Use object-oriented design: have classes, methods and utilize instance properties and

methods. o There should be little use of static variables and methods only when specified.

 Passing data between classes should either be done using using methods (depending on direction of data transmission).

o Data variables should not be made public/static to allow access to variables from other classes

<ul>

 <li>  Submit the project to Blackboard as a zip file, named in the format: “&lt;YourName&gt;Project.zip.” All students must submit the project individually.</li>

 <li>  Follow the CIS 340 Programming Conventions and CIS340 Commenting Guide documents for producing good, readable, and easily maintainable code.
 Feature Requirements
 You have the freedom to visually structure your application according to your preference. All applications should allow users to:</li>

 <li>  Can log into multiple customer accounts containing different data</li>

 <li>  View GetMoney’s available cash on hand and track changes as transaction occur</li>

 <li>  Perform the following operations:</li>

</ul>

o View account balance  Account with credit that owes no money  Account that owes money  Account at or near credit limit  Account with huge credit big enough to try and borrow all available cash

o Borrow and Payback amounts (need to perform 5 mixing and matching)  Verify 10% fee is applied and updates both account balance and cash available

o Ensure only 5 transactions are allowed o Change customer information (each item) and after changes see if login still works o View transaction history to ensure it updates correctly

<ul>

 <li>  Enter bad data to ensure program does not crash due to exceptions</li>

 <li>  Login and out of a customer account making transactions and ensure on a subsequent login all
 account balance modifications are saved.</li>

 <li>  Use admin login to exit program
 Technical Requirements:</li>

 <li>  Use the namespace: GetMoney</li>

 <li>  The project should have at minimum the classes with their corresponding data and
 functionality listed above. You are free to have more classes if suitable.</li>

 <li>  The project should start up with test data that will be provided. When the project starts, it will
 contain customers (1 must be you) already written in the code.</li>

 <li>  The class project is meant to be a demonstration of concepts learned in class. It is a technical
 requirement that the classes, statements, loops, and methods covered in class be utilized for this project.</li>

</ul>

o Barring small methods not covered in class, concepts not covered in class should not be used for the project.

o No credit will be given for code, which significantly departs from class concepts and utilizes data structures, tools, controls, and techniques not covered in class.