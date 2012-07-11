# Gist-From-CommandLine
This is a simple **python** script that can make you post gists from the command line. I have only tested the script on linux systems. Probably it should work under windows also but in that case you may have to do slight modifications like changing the '\n' used in the script with '\r\n' since windows terminal end the input with a carriage return and a newline character ( I am not sure about it)

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

or you can also use pipelines with this as :
- `cat harry.txt | gistcli` # Takes data from the pipeline.

**Note :** You should'nt use the '-f' flag with gistcli when using the pipeline, but even if you do, the preference is given to the data taken from the file mentioned, not the pipeline.


- `gistcli -f harry.txt -d 'Python multithreading example.'` # Returns a link of the **public** gist with **description** `Python multithreading example.`
- `gistcli -f harry.txt -d 'Python multithreading example.' -p` # Returns a **private** gist like above.

You can also use the terminal standard input to post that entered data as a gist. In that case, to stop reading data from the terminal just enter "."(quotes for clarity) in the last line of your input. (Don't worry that "." won't be included in your gist.)

## Problems that you might face
Presently I have assumed that your python interpreter is in the path `/usr/bin/python`. If your distribution has any other path then you just need to change the first line of the script to the path of the interpreter.

# Scope
- Currently only anonymous gists are posted to github via this tool. The script needs to be extended for adding authentication for user based gists.


