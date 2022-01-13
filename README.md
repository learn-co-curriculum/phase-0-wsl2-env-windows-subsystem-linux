# Setting Up WSL2

Windows Subsystem Linux (WSL) is **not** automatically enabled on windows. So,
to start, we need to enable it!

## Install Windows Subsystem for Linux (WSL) and Ubuntu

Now that we know your computer is ready for the rest of the environment setup,
we can install Windows Subsystem for Linux (WSL) and the Ubuntu Linux
distribution. You'll be doing the majority of your dev work using WSL and
Ubuntu, so this step is critical to complete before moving ahead.

### Action Item: Install WSL Features

1. Search for the "Command Prompt" application using the "Start" menu
2. Select "Run as administrator" from the right side of the search window
3. Allow the program to make changes to your device and wait for the "Command
   Prompt" application to open
4. Type `wsl --install -d Ubuntu` and press `<Enter>`
5. The terminal should output "The requested operation is successful."
6. Restart your computer to complete the installation.

> **Note:** If you encounter an error message that says "Ubuntu required feature
> not installed" then try enabling VSM in your BIOS. Follow
> [this guide](https://bce.berkeley.edu/enabling-virtualization-in-your-pc-bios.html) 
> to access your BIOS and get to the virtualization settings. Enable VSM and
> virtualization options from there. Check out
> [this issue](https://github.com/microsoft/>WSL/issues/5689) for reference.

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/w01AU7pl24w" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Action Item: Install the "Ubuntu" Application

You are ready to install and set up the Ubuntu operating system! Ubuntu is a
Linux-based operating system and this is the application we'll use to run the
remainder of the environment setup.

1. Open the "Microsoft Store" application using the "Start" menu
2. Search for "Ubuntu" _(Note: do not choose "Ubuntu 16.04 LTS", "Ubuntu 18.04
   LTS", or "Ubuntu 20.04LTS". Instead, choose the option that has no number
   next to it.)_
3. Click "Get" and "Install" and wait for the application installation to complete
4. Open the "Ubuntu" application
5. When it says "Enter new UNIX username:" add a simple username and press
   `<Enter>` (Note: usernames may not start with a number, and may not include
   capital letters)
6. Where it says "New password:" add a simple password and press `<Enter>` _(Note:
   you will not see any text when you are typing your password.)_
7. Where it says "Retype new password:" retype the same password from before and
   press `<Enter>` _(Note: store this password somewhere safe. You will need it to
   be able to run commands in the future)_
8. The terminal should output "Installation successful!" and then print about 50
   lines that you can ignore

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/cmLjpYx1Ys8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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
   _(Note: you should see a message starting with "For information on key
   differences…")_
5. Type `wsl --status` into the terminal and press `<Enter>`. You should see a
   message including "Default Version 2", which verifies that the default
   version has been set correctly.
6. Type `wsl --set-version Ubuntu 2` into the terminal and press `<Enter>`
7. Wait for the "Conversion complete" or "This distribution is already the
   requested version" message in the terminal
8. Type `wsl --list --verbose` into the terminal and press `<Enter>`. You should
   see a message including "NAME Ubuntu VERSION 2", which verifies that the
   default version has been set correctly.

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/Thy8DJEb7Pk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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
6. If the dropdown in your terminal says "1: wsl", continue to step 9.
   Otherwise, click on the dropdown in the terminal that says "1: powershell"
   and choose "Select Default Profile"
7. A dropdown should appear at the top of your VS Code window
8. Click on "Ubuntu (WSL)" to enable VS Code to display your Ubuntu terminal
9. Close the "Visual Studio Code" application
10. Open the "Ubuntu" application using the "Start" menu
11. Type `code` and press `<Enter>`

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/UasRLsxCFRQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

If the "Visual Studio Code" application opens when you type `code` in the
"Ubuntu" application, continue to the next lesson, **Installing Node on WSL2**.
