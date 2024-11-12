# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file
Save each script in a file with a .bat extension.
Ensure you have the necessary permissions to perform the operations.
Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 

# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "MyLab" on the desktop.
## COMMAND AND OUTPUT
```
mkdir %userprofile%\Desktop\MyLab
```
![image](https://github.com/user-attachments/assets/5070f0a9-92d4-4bd0-be8d-db06ed854b23)

Change to the "MyLab" directory and create an empty text file named "MyFile.txt" inside it.

## COMMAND AND OUTPUT
```
cd %userprofile%\Desktop\MyLab
```
![image](https://github.com/user-attachments/assets/25f53730-f910-4a19-b2de-bd4e7e5abb11)

```
type nul > MyFile.txt
```
![image](https://github.com/user-attachments/assets/1503cf5d-1942-40b1-a253-217cee4cc3ac)

List the contents of the "MyLab" directory.

## COMMAND AND OUTPUT
```
dir %userprofile%\Desktop\MyLab
```
![image](https://github.com/user-attachments/assets/247afe97-2cbd-45da-88d8-8f8511a4df8f)

Copy "MyFile.txt" to a new folder named "Backup" on the desktop.

## COMMAND AND OUTPUT
```
mkdir %userprofile%\Desktop\Backup
```
![image](https://github.com/user-attachments/assets/6fee9bee-d7c7-4db3-81fd-4643e99d6e4d)
```
copy MyFile.txt %userprofile%\Desktop\Backup
```
![image](https://github.com/user-attachments/assets/064ed5d7-be47-42d1-8e53-0862e65045e5)

Move the "MyLab" directory to the "Documents" folder.

## COMMAND AND OUTPUT
```
mkdir %userprofile%\Desktop\Documents
move MyLab Documents
```
![image](https://github.com/user-attachments/assets/798979ec-6b79-4a27-b9ef-159c22f3b22a)


## Exercise 2: Advanced Batch Scripting
Create a batch script named "BackupScript.bat" that creates a backup of files with the ".docx" extension from the "Documents" folder to a new folder named "DocBackup" on the desktop.
```
@echo off
mkdir %userprofile%\Desktop\DocBackup
copy %userprofile%\Documents\*.docx %userprofile%\Desktop\DocBackup
echo Backup completed successfully!
```

![image](https://github.com/user-attachments/assets/918014d8-5c48-4c0e-93ed-93b97c62472b)


## COMMENT:
```
@echo off
mkdir %userprofile%\Desktop\DocBackup
copy %userprofile%\Documents\*.docx %userprofile%\Desktop\DocBackup
del %userprofile%\Documents\*.docx
echo Backup and deletion completed successfully!
```
## OUTPUT
![Uploading image.png…]()


# RESULT:
The commands/batch files are executed successfully.

