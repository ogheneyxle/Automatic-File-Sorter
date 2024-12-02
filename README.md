# Automatic-File-Sorter

## Project Overview
The aim of this project is to show how one can use python to automatically sort files into folders using their extension/format. It is pretty straightforward, and the code does just that, it takes files and places them into folders per the instructed location.

## Tools
- Jupyter Notebook

## Brief Walkthrough
- To start, we must first import the operating system and initiate 'shutil' so we can easily manipulate files on the machine
```
importos, shutil
```

- Then, assess your computer, where are these files you want sorted? when you find the directory location, copy it and paste onto a cell.
- Next, since the file path you copied is lenghty, you need to assign it to a shorter variable. I chose 'path'
```
path = r'C:/Users/user/Desktop/python file sorter/'
```

- Also, change the '\' to '/' and place 'r' before the directory info so it is treated as a raw string
- Next, create folder names you want per the file types and create a 'for loop' statement to assign them names
```
folder_names = ['excel files','image files','video files','pdf files']

for loop in range(0,4):
    if not os.path.exists(path + folder_names[loop]):
       print(path + folder_names[loop])
       os.makedirs(path + folder_names[loop])
```
- Finally, using if/elif/else statements, you can sort the files according to their format/extension. Take note to input the correct file format in the command, for example;

```
for file in file_name:
    if ".xlsx" in file and not  os.path.exists(path + 'excel files/' + file):
        shutil.move(path + file, path + 'excel files/' + file)
```
Repeat the above line of code, switching out the file type to whichever you want to sort. 
🃏
