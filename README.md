# Gist-From-CommandLine
This is a simple **python** script that can make you post gists from the command line.

# Requirements 
Only requirement is that you should have python 2.7 installed on your system. (Though slight modification should make it run on python3 too.)

# Usage
Make the script executable (as `chmod +x gistcli`) and add the script to your PATH variable or you can create a symlink to your script in your PATH directory. Now you should be able to use gistcli command directly from your terminal. 

For more information you can see the inbuilt help of gistcli (gistcli -h).

# Examples
Following examples should help you to have quick grasp of the script functionality.
Assume that filename is `harry.txt`.

#### Minimalistic Usage
- `gistcli -f harry.txt`  # Returns a link of the **public** gist with **description** `Gist - Paste`.


- `gistcli -f harry.txt -d 'Python multithreading example.'` # Returns a link of the **public** gist with **description** `Python multithreading example.`
- `gistcli -f harry.txt -d 'Python multithreading example.' -p` # Returns a **private** gist like above.

## Problems that you might face
Presently I have assumed that your python interpreter has the path `/usr/bin/python`. If your distribution has any other path then you just need to change the first line of the script to the path of the interpreter.


