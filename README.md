# Linux Shell in C 

## Steps to compile:
1. Run make command
2. Type ./shell 
3. Run any command in the shell
4. In order to exit, run `quit`

## Built-in commands

1. `pwd`\
    Displays the name of the working directory.

2. `ls [-l -a] [directory]`\
    Variations such as `ls, ls . , ls ..` also work\
    Also handles multiple directories as arguments. eg. `ls -l dir1 dir2 dir3`

3. `cd [file]`\
    Changes directory to the directory specified, throws an error if the directory does not exist

4. `echo [arguments]`\
    Displays whatever is specified in [arguments]

5. `quit`\
    Exits the shell

6. `setenv var[value]` & `unset var`\
    Creates an enviornmental variable `var` if it doesn't already exist and assigns it the value given\
    `unset var` destroys that environmental variable

7.  `jobs`\
    Prints a list of all currently running jobs along with their pid in order of their creation

8. `kjob <jobNumber> <signalNumber>`\ 
    Takes the job id of a running job and sends a signal value to that process

9. `fg <jobNumber>`\
    Brings a running or a stopped background job with given job number to foreground

10. `bg <jobNumber>`\
    Changes a stopped background job to a running background job

11. `overkill`\
    Kills all background process at once


### Foreground and Background Processes
    All other commands are treated as system commands like emacs, vim etc
    To run a process in the background, follow the command with a '&' symbol. Eg. `emacs &`
    Upon termination of a background process, the shell prints its PID

### Additional Commands

1. `pinfo [PID]`\
    Prints numerous details about the process such as its status, memory, and executable path
    Just `pinfo` with no arguments gives details of the shell

## Other Features

1. `​CTRL-Z`\
    Changes the status of currently running job to stop, and pushes it to the background

2. `CTRL-C`\
    Sends SIGINT signal to the current foreground job of the shell​
    If there is no foreground job, then the signal does not have any effect

3. `CTRL-D`\
    quits shell

4. Input-Output Redirection & Piping\
    Handles `<`, `>`, `>>`, and `|` operators appropriately, wherever they are in the command
    Throws error if syntax is incorrect

## Files:

Makefile - code to compile various files\
ls.c - implements ls\
pwd.c - implements pwd\
echo.c - implements echo\
cd.c - implements cd\
readline.c - reads input from shell\
splitline.c - splits and tokenizes input into various arguments\
prompt.c - prints prompt on shell(display requirement)(main shell loop)\
execute.c - executes foreground and background processes\
pinfo.c - implements pinfo command \
shell.h - contains function definitions and various header files\
signal_handler.c - signal handling i.e ctrl-c and ctrl-z\
setenv.c - implements setenv and unsetenv\
redirection_piping.c - implements piping + io redirection\
overkill.c - implements overkill command\
quit.c - implements quit command\
pipe.c - implements piping\
kjob.c - implements kjob command\
jobs.c - implements jobs command\
io_redirection.c - implements io redirection\ 
fg.c - implements fg command\
bg.c - implements bg command