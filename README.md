# conditional statement

<h1>Activity: Create a conditional statement</h1>

<h1>Introduction</h1>

Conditional statements are a powerful structure that help in achieving automation when you need to make sure conditions are met before certain actions are executed. For example, security analysts can use 
conditional statements in Python to check if users are approved to access a device.

In this lab, you will practice writing conditional statements in Python.

<h1>Scenario</h1>
You're working as a security analyst. First, you are responsible for checking whether a user's operating system requires an update. Then, you need to investigate login attempts to a specific device. You must determine if login attempts were made by users approved to access this device and if the login attempts occurred during organization hours.

<h1>Task 1</h1>
You are asked to help automate the process of checking whether a user's operating system requires an update. Imagine that a user's device can be running one of the following operating systems: OS 1, OS 2, or OS 3. While OS 2 is up-to-date, OS 1 and OS 3 are not. Your task is to check whether the user's system is up-to-date, and if it is, display a message accordingly. To do this, complete the conditional statement using the keyword if. Be sure to replace the ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/95f81f8c-608d-4ee9-a90a-9a4d0aa3f746)

<H1>Task 2</H1>
Now try assigning the system variable to different values ("OS 1", "OS 2", and "OS 3"), run the cell, and observe what happens. Keep the conditional statement as is. Be sure to replace the ### YOUR CODE HERE ### with your own code.

![image](https://github.com/user-attachments/assets/d8b31417-0207-46f5-8e82-b3a8389e1cbc)

<H1>Question 1</H1>
What happens when OS 2 is running? What happens when OS 1 is running?

When OS 2 is running, no update needed is displayed. When OS 1 is running, nothing is displayed. The print statement above is only executed when the condition system == "OS 2" evaluates to True.

<H1>Task 3</H1>
Nothing is displayed when the system is not equal to "OS 2". This is because the condition didn't evaluate to True.

It would be beneficial if an alternative message is provided to them when updates are needed.

In the following cell, add the appropriate keyword after the first conditional so that it will display a message that conveys that an update is needed when the system is not running OS 2. Be sure to replace each ### YOUR CODE HERE ### with your own code.

Then, set the value of the system variable to indicate that OS 2 is running and run the cell. After observing what happens, set the value of system to indicate either that OS 1 is running or that OS 3 is running and run the cell.

![image](https://github.com/user-attachments/assets/04824593-a3c9-423c-94c5-b98e1b8715ef)

<H1>Question 2</H1>
In this setup what happens when OS 2 is running? And what happens when OS 2 is not running?

In this setup, when OS 2 is running, no update needed is displayed. And when OS 2 is not running, update needed is displayed.

<H1>Task 4</H1>
This setup is still not ideal. If the variable system contains a random string or integer, the conditional above would still display update needed.

To improve the conditional, you will need to add the elif keyword. In the following cell, you will add two elif statements after the if statement, to create the final code. The first elif statement will display update needed if system is "OS 1". The second elif statement will display the same message, if system is "OS 3". Complete the second elif statement, and then run the cell with the variable system set to a different string each time. Observe what happens when each operating system is running. Also try assigning the system variable to some strings other than "OS 1", "OS 2", and "OS 3" (for example "OS 4").

Be sure to replace each ### YOUR CODE HERE ### with your own code.

![image](https://github.com/user-attachments/assets/4af3c91d-93c0-4308-a935-81a88610e2df)

<h1>Question 3</h1>
Under this setup what happens when OS 2 is running? What happens when OS 1 is running? What happens when OS 3 is running? What happens when neither of those three operating systems are running?

Under this setup, when OS 2 is running, no update needed is displayed. When either OS 1 or OS 3 is running, update needed is displayed. When neither of those three operating systems are running, nothing is displayed.

<H1>Task 5</H1>
Writing code that is readable and concise is a best practice in programming.

The conditional above can be written more concisely.

In the following cell, use a logical operator to combine the two elif statements from the previous setup into one elif statement. Be sure to replace each ### YOUR CODE HERE ###. Then, assign the system variable to a value and run the cell. Like you did in the previous task, use "OS 1", "OS 2", "OS 3", and other strings.


![image](https://github.com/user-attachments/assets/3de37eac-626b-46d4-8c05-3c8073cf8f01)

<h1>Question 4</h1>
What do you observe about this conditional?

This conditional behaves the same way as the previous conditional. The only difference is that the syntax in this conditional is more concise. The use of the or operator allows you to combine the two conditions into one elif statement, which is more concise than having the two separate elif statements that were written previously.

<h1>Task 6</h1>
Now you'll move on to the next part of your work. You've been asked to investigate login attempts to a specific device. Only approved users should log on to this device.

You'll start with two authorized users, stored in the variables approved_user1 and approved_user2. You'll need to write a conditional statement that compares those variables to a third variable, username. This will be the username of a specific user trying to log in. Be sure to replace each ### YOUR CODE HERE ### with your own code.

![image](https://github.com/user-attachments/assets/58015829-96a6-4652-bf1b-87e53bd2111f)

<h1>Task 7</h1>
The number of approved users has now expanded to five. Rather than storing each of the approved users' usernames individually, it would be more concise to store them in an allow list called approved_list.

The in operator in Python can be used to determine whether a given value is an element of a sequence. Using the in operator in a condition can help you check whether a specific username is part of a list of approved usernames. For example, in the code below, username in approved_list evaluates to True if the value of the username variable is included in approved_list.

Complete the code in the following cell to display the same messages that you used in the previous step. When the condition evaluates to True, the following message will be displayed: "This user has access to this device." When it evaluates to False, the following message will be displayed: "This user does not have access to this device." Then, run the cell to observe its behavior. Be sure to replace each ### YOUR CODE HERE ### with your own code. Afterwards, reassign the username variable to a username that is not approved and run the cell to observe what happens.

![image](https://github.com/user-attachments/assets/3d73d098-9d24-43d2-bb3f-0f8235519028)

<h1>Question 5</h1>
What happens when an approved user tries to log in? What happens when an unapproved user tries to log in?

When an approved user tries to log in, "This user has access to this device." is displayed. When an unapproved user tries to log in, "This user does not have access to this device." is displayed.

<h1>Task 8</h1>
Now you'll write another conditional statement. This one will use a organization_hours variable to check if the user logged in during specific organization hours. When that condition is met, the code should display the string "Login attempt made during organization hours.". When that condition isn't met, the code should display the string "Login attempt made outside of organization hours.".

The organization_hours variable will have a Boolean data type. If organization_hours has a Boolean value of True, that means the user is logged in during the specified organization hours. If organization_hours has a Boolean value of False, that means the user is not logged in during those hours.

Complete the conditional in the following cell. Be sure to replace each ### YOUR CODE HERE ### with your own code before running the following cell.

![image](https://github.com/user-attachments/assets/167d419a-5257-4585-b053-83932313ce63)

<h1>Question 6</h1>
What happens when the user logs in during organization hours? What happens when they log in outside of organization hours?

When the user logs in during organization hours, the condition in the if statement evaluates to True, and a message about login attempt during organization hours is displayed. When the user logs in outside of organization hours, the condition in the if statement evaluates to False. This means the else statement is executed, and a message about login attempt outside of organization hours is displayed.

<h1>Task 9</h1>
The following cell assembles the code from the previous tasks. It includes the conditional statement that checks if a user is on the allow list and the conditional statement that checks if the user logged in during organization hours.

Run the cell below a few times. Each time, enter a different combination of values for username and organization_hours to observe how that affects the output.

![image](https://github.com/user-attachments/assets/62869c83-c7e4-4990-b3b3-06d0e34083d4)

<h1>Question 7</h1>
What happens when the user trying to log in is not among the approved users? What happens when the user trying to log in is among the approved users? What happens when the user tries to log in outside of organization hours?

When the user trying to log in is not among the approved users, a message is displayed about the user not having access to the device. The code then goes on to check whether the user attempted to log in during organization hours.

When the user trying to log in is among the approved users, a message is displayed about the user having access to the device and then the code checks whether they attempted to log in during organization hours. When the user trying to log in is doing so outside of organization hours, a message is displayed about login attempt outside of organization hours.

<h1>Task 10</h1>
You can also provide a single message about the login attempt. To do this, you can join both conditions into a single conditional statement using a logical operator. This will make the code more concise.

Examine the code in the following cell and add the missing operator that would allow for a single message. Be sure to replace each ### YOUR CODE HERE ### with your own code before running the following cell. Then run the cell, entering different combinations of information, and observe what happens.

![image](https://github.com/user-attachments/assets/c0004e67-d0b8-4981-9bba-d625b5c49593)

<h1>Question 8</h1>
In this setup, what happens when the user trying to log in is an approved user and doing so during organization hours? What happens when the user either is not approved or attempts to log in outside of organization hours?

In this setup, when the user is approved and attempts to log in during organization hours, the message "Login attempt made by an approved user during organization hours." is displayed. If the user is either not approved or attempts to log in outside of organization hours, the message "Username not approved or login attempt made outside of organization hours." is displayed. This code checks the same conditions as the code in the previous task. However, it joins them into one if statement, and both username and organization_hours are investigated before a single message is displayed.

<h1>Conclusion</h1>
What are your key takeaways from this lab?

- Conditional statements, comparison operators, and logical operators play a major role in automating important processes to maintain security, such as detecting when a user's operating system requires updates and detecting when a user is allowed to access a device.
- Conditional statements allow you to determine whether a specific set of conditions has been met.
- Comparison operators allow you to compare pairs of values. Specifically, the == operator allows you to determine whether one value is equal to another.
- Logical operators such as and and or allow you to check more than one condition at a time.

