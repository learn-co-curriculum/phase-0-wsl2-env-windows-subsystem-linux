# Setting Up WSL2

Windows Subsystem for Linux (WSL) is **not** automatically enabled on Windows.
So, to start, we need to enable it!

## Install Windows Subsystem for Linux (WSL) and Ubuntu

Now that we know your computer is ready for the rest of the environment setup,
we can install Windows Subsystem for Linux (WSL) and the Ubuntu Linux
distribution. You'll be doing the majority of your dev work using WSL and
Ubuntu, so this step is critical to complete before moving ahead.

### Action Item: Install WSL and Ubuntu

1. Open the "Command Prompt" application using the "Start" menu
2. Type `wsl --install -d Ubuntu` and press `<Enter>`
3. Once "Ubuntu" has been installed, the `Ubuntu` application will open in a new
   window
4. In the "Ubuntu" application, when it says "Enter new UNIX username:" add a
   simple username and press `<Enter>` _(Note: usernames may not start with a
   number and may not include capital letters. It does not need to be the same
   as your Windows username.)_
5. Where it says "New password:" add a simple password and press `<Enter>`
   _(Note: you will not see any text when you are typing your password.)_
6. Where it says "Retype new password:" retype the same password from before and
   press `<Enter>` _(Note: store this password somewhere safe. You will need it
   to be able to run commands in the future)_
7. The terminal should output "Installation successful!" and then print about 50
   lines that you can ignore

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/tUZ73za0Q70" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Now, the last line in your "Ubuntu" application should say your username +
"@DESKTOP" + some random numbers and letters. If you see that, continue below.

## Update the Windows Subsystem for Linux (WSL) to WSL 2

Now that we have the Windows Subsystem for Linux (WSL) enabled and we have the
"Ubuntu" application installed, we can update WSL to version 2 and update the
"Ubuntu" application to use WSL 2.

### Action Item

1. Search for the "Command Prompt" application using the "Start" menu
2. Select "Run as administrator" from the right side of the search window
3. Allow the program to make changes to your device and wait for the "Command
   Prompt" application to open
4. Type `wsl --set-default-version 2` into the terminal and press `<Enter>`
   (Note: you should see a message starting with "For information on key
   differences…")
5. Type `wsl --set-version Ubuntu 2` into the terminal and press `<Enter>`
6. Wait for the "Conversion complete" or "This distribution is already the
   requested version" message in the terminal

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/gxvMznj-2Vs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

If you saw the "Conversion complete" or "This distribution is already the
requested version" message in the "Command Prompt" application, close the
"Command Prompt" application and continue below.

> **Note:** If you encounter an error message that you need to enable the
> Virtual Machine Platform, but you've already enabled it, you may not be able
> to use WSL2. However, you may still be able to use WSL1. Run
> `wsl --set-default-version 1`, then run `wsl --set-version Ubuntu 1`. Wait for
> the "Conversion complete" or "This distribution is already the requested
> version" message in the terminal, then continue on with these instructions.

## Configure VS Code to Work with WSL

### Action Item

1. Open the "Visual Studio Code" application using the "Start" menu
2. Click "View" in the toolbar, then click "Extensions" in the dropdown menu, or
   use the shortcut `<Control>` + `<Shift>` + `X`
3. Search for "Remote - WSL" and click on the item in the list with the same
   name (Note: the description should start with "Open any folder in the Windows
   Subsystem for Linux (WSL) …")
4. Click the "Install" button near the top of the page
5. Click "Terminal" in the toolbar, then click "New Terminal" (Note: a new
   terminal should appear at the bottom of your VS Code window)
6. Click on the dropdown in the terminal that says "1: powershell" and choose
   "Select Default Profile"
7. A dropdown should appear at the top of your VS Code window
8. Click on "Ubuntu (WSL)" to enable VS Code to display your Ubuntu terminal
9. Close the "Visual Studio Code" application
10. Open the "Ubuntu" application using the "Start" menu
11. Type `code` and press `<Enter>`

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/46JONhRYc1I" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

If the "Visual Studio Code" application opens when you type `code` in the
"Ubuntu" application, continue to the next lesson, **Installing Node on WSL2**.
