<!-- TITLE -->

# Email Slicer Using Python

Email Slicer is a simple tool where the email address is provided as an input and the application returns the username and the domain of the email address as an output. It makes use of the slicing operation in Python.

<!-- BUILT WITH -->

## Built With

![Python][python-shield]

<!-- EXAMPLE -->

## Example

Input:
```
Please enter your Email Id:
gargaviral99@gmail.com
```

Output:
```
Your username is: gargaviral99
Your domain is: gmail.com
```

Here we got **`gargaviral99`** as username and **`gmail.com`** as domain.

<!-- INSTALLATION -->

## Installation

Use the link to download Python.

[![Python][python-shield]][python-url]

Use the link to download Visual Studio Code.

[![Visual Studio Code][visual studio code-shield]][visual studio code-url]

<!-- USAGE -->

## Usage

Open Command Prompt or Windows PowerShell to start.

```python
# get into python mode
python

# create a python script
hello.py
print("Hello World")

# go to the file path
cd <file path>

# run the script
python hello.py
```

VS Code or PyCharm can also be used.

<!-- CODE -->

## Code

So at first we are going to ask the user to enter the email that is to be sliced.

```python
print("Please enter your Email Id:")
email = input().strip()
```

Here, as usual, we are making use of the **`input()`** function to get the input from the user in form of a string. We will store this input string in **`email`** variable.

Also we are making use of the **`strip()`** function. **`strip()`** function will remove any additional & unwanted spacing on both sides of the input string. So that we can make sure that we have only the email in the input and not any unwanted spaces.

```python
if email.find("@") != -1:
```

Here we are checking if the input string contains **`@`** or not. If it contains **`@`**, then it is considered as a valid email id and we move to the next step, which is slicing the email.

```python
username = email[:email.index("@")]
domain = email[email.index("@") + 1:]
```

Now, we print the **`username`** and **`domain`** to show the result.

```python
print("Your username is: ", username)
print("Your domain is: ", domain)
```

If the input string does not contain **`@`**, then it is considered as an invalid email id and we get out of the loop with a warning message.

```python
else:
     print("Please enter a valid Email Id.")
```

<!-- LOGIC -->

## Logic

Let's consider the input is **`avimax37@gmail.com`**, so when we write **`email[email.index("@"):]`**, our **`index()`** function will interpret it as **`email[:8]`** as our **`@`** is located at index **8**. Now **`email[:8]`** knows that **`@`** is located at index **8**, so now it will keep the part before index **8** and discard the rest. It will store the stripped value in **`username`**.

This exact same process is followed for **`domain`** also.


