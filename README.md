Linux Shell in C 

Steps to compile:
1. Run make command
2. Type ./shell 

Files:

Makefile - code to compile various files
ls.c - implements ls
pwd.c - implements pwd
echo.c - implements echo
cd.c - implements cd
readline.c - reads input from shell
splitline.c - splits and tokenizes input into various arguments
prompt.c - prints prompt on shell(display requirement)(main shell loop)
execute.c - executes foreground and background processes
pinfo.c - implements pinfo command 
shell.h - contains function definitions and various header files
signal_handler.c - signal handling i.e ctrl-c and ctrl-z
setenv.c - implements setenv and unsetenv
redirection_piping.c - implements piping + io redirection
overkill.c - implements overkill command
quit.c - implements quit command
pipe.c - implements piping
kjob.c - implements kjob command
jobs.c - implements jobs command
io_redirection.c - implements io redirection 
fg.c - implements fg command
bg.c - implements bg command
