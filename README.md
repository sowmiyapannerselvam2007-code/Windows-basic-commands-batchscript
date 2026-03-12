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
<img width="971" height="587" alt="Screenshot 2026-03-12 162806" src="https://github.com/user-attachments/assets/c565ff89-7b89-41af-b925-5088290d1834" />

## COMMAND AND OUTPUT
<img width="1029" height="152" alt="Screenshot 2026-03-12 162821" src="https://github.com/user-attachments/assets/d423959d-3354-4208-9bda-102525423e3a" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT

<img width="571" height="147" alt="Screenshot 2026-03-12 162831" src="https://github.com/user-attachments/assets/a012c761-c9d1-4d16-ad9f-cddfdc2384da" />

Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="561" height="137" alt="Screenshot 2026-03-12 162840" src="https://github.com/user-attachments/assets/585e8927-658b-42e4-afe2-bc2ba2b49f4e" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="567" height="168" alt="Screenshot 2026-03-12 162850" src="https://github.com/user-attachments/assets/c95a9742-3a16-417a-8140-ac746d2fc17e" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="1037" height="218" alt="Screenshot 2026-03-12 164312" src="https://github.com/user-attachments/assets/bcd69483-f715-4a21-9b1d-76cade15ba84" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="775" height="93" alt="Screenshot 2026-03-12 164342" src="https://github.com/user-attachments/assets/db4ced13-7332-40fc-926a-c537b156cca3" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="1038" height="126" alt="Screenshot 2026-03-12 164327" src="https://github.com/user-attachments/assets/423286f0-5717-40fe-b0fd-c8f997049c29" />

List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="775" height="93" alt="Screenshot 2026-03-12 164342" src="https://github.com/user-attachments/assets/b42a0a09-cd39-4844-8080-4949b34f0b05" />

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="732" height="158" alt="Screenshot 2026-03-12 164441" src="https://github.com/user-attachments/assets/04510262-2a7a-4043-85f2-7d0bce9457f0" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=Saveetha
echo Hello, %name%!
pause
```
## OUTPUT
<img width="474" height="100" alt="Screenshot 2026-03-12 165352" src="https://github.com/user-attachments/assets/3719d18b-348e-4928-a4b0-2f5ca587549e" />



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
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
```

## OUTPUT
<img width="754" height="213" alt="Screenshot 2026-03-12 165620" src="https://github.com/user-attachments/assets/6fc1c12b-34ee-4cc2-a674-a0acdb658c60" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## OUTPUT


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```

@echo off
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
pause
```

## OUTPUT
![Uploading Screenshot 2026-03-12 165746.png…]()



# RESULT:
The commands/batch files are executed successfully.
The commands/batch files are executed successfully.

