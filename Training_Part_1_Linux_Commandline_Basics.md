# Training Part 1 -- Linux Command line basics

### BASIC LINUX COMMANDS

Here is a short list of basic, but essential commands. In Linux, commands are case-sensitive and more often than not they are entirely in lowercase. Items that are surrounded by brackets ([]) are optional. 

You will use ls to display information about files and directories.
```
ls
```

Changes the current directory to dir. If you execute cd without specifying a directory, cd changes the current directory to your home directory. This is how you navigate around the system.
```
cd [dir]
```

Displays the present working directory name. If you don't know 
what directory you are in, pwd will tell you.
```
pwd
```

Concatenates and displays files. This is the command you run to view the contents of a file.
```
cat [file]
```

Displays arguments to the screen.
```
echo [argument]
```

## Working with files and directories




## [Exercise 1]



## Piping in Linux 
The Linux systems allow the stdout of a command to be connected to the stdin of another command. You can make it do so by using the pipe character '|'. 
This direct connection between commands/ programs/ processes allows them to operate simultaneously and permits data to be transferred between them continuously rather than having to pass it through temporary text files or through the display screen. 
Pipes are unidirectional i.e., data flows from left to right through the pipeline. 

**Syntax**
```
command_1 | command_2 | command_3 | .... | command_N 
```