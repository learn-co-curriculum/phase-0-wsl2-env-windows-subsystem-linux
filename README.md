# Setting Up WSL2

Windows Subsystem Linux (WSL) is **not** automatically enabled on windows. So,
to start, we need to enable it!

## Enable the Windows Subsystem for Linux (WSL) and Virtual Machine Platform

Now that we know your computer is ready for the rest of the environment setup,
we need to enable two more settings before moving on. We’ll be using the Windows
Subsystem for Linux (WSL) and the Virtual Machine Platform to create a space on
our computer for our Ubuntu operating system.

### Action Item: Enable Windows Subsystem for Linux (WSL) and Virtual Machine Platform Settings

1. Open the "Turn windows features on and off" application using the "Start"
   menu
2. Check the box next to "Virtual Machine Platform"
3. Check the box next to "Windows Subsystem for Linux"
4. Click "OK" to save your work; your computer should restart

### Check Your Work

If you can check both of those checkboxes and your computer restarts, continue
below. Otherwise, reach out to your teaching team for next steps.

## Set up the "Ubuntu" Application

After you have installed the "Ubuntu" application from the Microsoft Store and
enabled Windows Subsystem for Linux (WSL) and the Virtual Machine Platform, we
have to set up the Ubuntu operating system.

### Action Item

1. Open the "Ubuntu" application using the "Start" menu
2. When it says "Enter new UNIX username:" add a simple username and press
   `<Enter>` _(Note: usernames may not start with a number, usernames may not
   include capital letters)_
3. Where it says "New password:" add a simple password and press `<Enter>`
   _(Note: you will not see any text when you are typing your password.)_
4. Where it says "Retype new password:" retype the same password from before and
   press `<Enter>`
5. The terminal should output "Installation successful!" and then print about 50
   lines that you can ignore

### Check Your Work

Now, the last line in your "Ubuntu" application should say your username +
"@DESKTOP" + some random numbers and letters. If you see that, continue below.

## Update the Windows Subsystem for Linux (WSL) to WSL 2

Now that we have the Windows Subsystem for Linux (WSL) enabled and we have the
"Ubuntu" application installed, we can update WSL to version 2 and update the
"Ubuntu" application to use WSL 2.

### Action Item

1. Download the WSL Update file by visiting the following webpage in your
   browser:
   https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
2. Open the file, follow the prompts, allow the program to make changes to your
   device, and click "Finish"
3. Search for the "Command Prompt" application using the "Start" menu
4. Select "Run as administrator" from the right side of the search window
5. Allow the program to make changes to your device and wait for the "Command
   Prompt" application to open
6. Type `wsl --set-default-version 2` into the terminal and press `<Enter>`
   (Note: you should see a message starting with "For information on key
   differences…")
7. Type `wsl --set-version Ubuntu 2` into the terminal and press `<Enter>`
8. Wait for the "Conversion complete" or "This distribution is already the
   requested version" message in the terminal

### Check Your Work

If you saw the "Conversion complete" or "This distribution is already the
requested version" message in the "Command Prompt" application, close the
"Command Prompt" application and continue below.

## Configure VS Code to Work with WSL

### Action Item

1. Open the "Visual Studio Code" application using the "Start" menu
2. Click "View" in the toolbar, then click "Extensions" in the dropdown menu, or
   use the shortcut `<Control>` + `<Shift>` + X
3. Search for "Remote - WSL" and click on the item in the list with the same
   name (Note: the description should start with "Open any folder in the Windows
   Subsystem for Linux (WSL) …")
4. Click the green "Install" button
5. Click "Terminal" in the toolbar, then click "New Terminal" (Note: a new
   terminal should appear at the bottom of your VS Code window)
6. Click on the dropdown in the terminal that says "1: powershell" and choose
   "Select Default Shell"
7. A dropdown should appear at the top of your VS Code window
8. Click on "WSL Bash" to enable VS Code to display your Ubuntu terminal
9. Close the "Visual Studio Code" application
10. Open the "Ubuntu" application using the "Start" menu
11. Type `code` and press `<Enter>`

### Check Your Work

If the "Visual Studio Code" application opens when you type `code` in the
"Ubuntu" application, continue to the next lesson, **Installing Ruby on WSL2**.
