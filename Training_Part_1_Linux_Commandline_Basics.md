# Training Part 1 -- Linux Command line basics

### Basic Linux Commands

Here is a short list of basic, but essential commands. In Linux, commands are case-sensitive and more often than not they are entirely in lowercase. Items that are surrounded by brackets (<>) are optional. 

You will use ls to display information about files and directories.
```
ls
```

Changes the current directory to dir. If you execute cd without specifying a directory, cd changes the current directory to your home directory. This is how you navigate around the system.
```
cd <dir>
```

Displays the present working directory name. If you don't know 
what directory you are in, pwd will tell you.
```
pwd
```

Concatenates and displays files. This is the command you run to view the contents of a file.
```
cat <file>
```

Displays arguments to the screen.
```
echo <argument>
```

## Working with directories and files

Linux directory structure is continuous, i.e. regardless of the
physical location of storage it all seems to be part of one
directory tree starting from root (/).

df  command tells how much disk space is available on various file
systems
```
df -h
```

Creating directory:

```
mkdir <dir_name>
```

Removing directory:

```
rmdir <dir_name>
```

There are many types of files. Here are the most important:
- Text files (human-readable; can be viewed and modified using a text
editor)
    - Text documents (e.g., README files)
    - Data in text format (e.g., FASTA, FASTQ, VCF, …)
- Scripts:
Shell scripts (usually *.sh or *.csh)
    - Perl scripts (usually *.pl)
    - Python scripts (usually *.py)

- Binary files (not human-readable; cannot be viewed using a text editor)
    - Executables (e.g., samtools, bwa, bowtie, firefox)
    - Data in binary format (e.g, BAM files, index files for BWA or Bowtie,
formatted BLAST databases)
    - Compressed files (usually *.gz, *.zip, *.bz2,…, but extensions
not necessary) – often text files re-formatted to save space on disk or
packaged directory trees

Creating an empty file (zero size):
```
touch <file_name>
```

Copying
```
cp <path_to_source> <path_to_destination>
```

Moving and/or renaming
```
mv <path_to_source> <path_to_destination>
```

Deleting
```
rm <path_to_file>
```

File and directory names – best practices
- Names are case-sensitive (MyFile, myfile, myFile are all different!)
- Use only letters (upper- and lower-case), numbers from 0 to 9, a dot (.),
and an underscore (_) [ good example: This_is_myFile99.abc]
- Avoid other characters, as they may have special meaning to either Linux,
or to the application you are trying to run. Do not use “space” or other
special characters [bad example: This is my&File#^99.abc ]
- Use of special characters in file names is possible if absolutely necessary,
but will lead to problems if done incorrectly.


## Piping in Linux 
The Linux systems allow the stdout of a command to be connected to the stdin of another command. You can make it do so by using the pipe character '|'. 
This direct connection between commands/ programs/ processes allows them to operate simultaneously and permits data to be transferred between them continuously rather than having to pass it through temporary text files or through the display screen. 
Pipes are unidirectional i.e., data flows from left to right through the pipeline. 

**Syntax**
```
command_1 | command_2 | command_3 | .... | command_N 
```

An example for counting lines, words, and characters:

```
cat <file.txt> | wc -l
```

This command lists all files and directories in the current directory, and then filters the output to only show items containing "txt" in their name. Sorting output with sort:

```
ls | sort
```