# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"
```
mkdir my-folder
```
<img width="665" height="28" alt="image" src="https://github.com/user-attachments/assets/f23b2943-a5ff-46b8-ba8d-114ff089c576" />

## COMMAND AND OUTPUT
Remove the directory "my-folder"
~~~
rmdir my-folder
~~~
![ooooo1](https://github.com/user-attachments/assets/60f6c58c-3c0b-47f5-b194-1a0c37bef999)

## COMMAND AND OUTPUT
Create the file Rose.txt
~~~
COPY CON Rose.txt
~~~
![ooooo3](https://github.com/user-attachments/assets/8a825ab4-bb30-4770-98c5-e40c80fa15d0)

## COMMAND AND OUTPUT
~~~
echo “hello world” > hello.txt
type hello.txt
~~~
![oooo4](https://github.com/user-attachments/assets/b12dafb3-a424-49a8-ac14-9b26da502c58)

Create the file hello.txt using echo and redirection


## COMMAND AND OUTPUT
~~~
copy hello.txt hello1.txt
~~~
![ooooo5](https://github.com/user-attachments/assets/481c2184-ad84-420b-a2bf-8c9b1242408b)


Copy the file hello.txt into the file hello1.txt
~~~
del hello1.txt
~~~
![oooo6](https://github.com/user-attachments/assets/d742e0eb-6dce-40c6-8422-be4fe1779439)


## COMMAND AND OUTPUT
~~~
dir hello1.txt
~~~
![oooo7](https://github.com/user-attachments/assets/248f52ff-cdc0-4f75-bb2c-918a62800c9e)


Remove the file hello1.txt

## COMMAND AND OUTPUT
~~~
assoc | more
~~~
![ooooo8](https://github.com/user-attachments/assets/761f4d48-e23f-47be-97d1-70038ec6d0fa)


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
~~~
fc hello.txt Rose.txt
~~~
![ooooo9](https://github.com/user-attachments/assets/fd984f54-8f8c-462e-b415-3de82568e04c)

List out all the associated file extensions 


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

~~~
@echo off
set name=John
echo Hello, %name%!
pause
~~~
## OUTPUT
![oooo10](https://github.com/user-attachments/assets/c36dcfb5-ab99-4be3-b17d-ad0d8f4fca29)



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
CODE:
~~~
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
~~~
## OUTPUT
![ooooo11](https://github.com/user-attachments/assets/1c0cf956-8433-45d6-a457-fddb8b307b3e)


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
CODE:
~~~
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
~~~
## OUTPUT
![oooo13](https://github.com/user-attachments/assets/a45931d3-c199-41da-849a-c8ccb546aa98)


Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
~~~
C@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pauseODE
~~~
## OUTPUT


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## OUTPUT

<img width="765" height="352" alt="image" src="https://github.com/user-attachments/assets/605f307b-a71f-4af0-8a1a-37b1f9c4ec9e" />


# RESULT:
The commands/batch files are executed successfully.

