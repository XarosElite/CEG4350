Jacob Poling
poling.47@wright.edu

total 860
-rw-rw-r-- 1 thonkerpad thonkerpad   1142 Oct  5 17:48 answers.txt
-rw------- 1 thonkerpad thonkerpad   2902 Oct  5 17:48 bitvector.cpp
-rw-rw-r-- 1 thonkerpad thonkerpad  23000 Oct  5 17:48 bitvector.o
-rw-rw-r-- 1 thonkerpad thonkerpad   8192 Oct  5 22:11 cmdsTried.txt
-rw------- 1 thonkerpad thonkerpad  65536 Oct  5 21:36 D1.dsk
-rw------- 1 thonkerpad thonkerpad 262144 Oct  5 17:48 D2.dsk
-rw------- 1 thonkerpad thonkerpad   5352 Oct  5 17:48 directory.cpp
-rw-rw-r-- 1 thonkerpad thonkerpad  30528 Oct  5 19:01 directory.o
-rw------- 1 thonkerpad thonkerpad    174 Oct  5 17:48 diskParams.dat
-rw------- 1 thonkerpad thonkerpad   4199 Oct  5 17:48 file.cpp
-rw-rw-r-- 1 thonkerpad thonkerpad  25968 Oct  5 17:48 file.o
-rw------- 1 thonkerpad thonkerpad   7000 Oct  5 17:48 fs33types.hpp
-rw-rw-r-- 1 thonkerpad thonkerpad  12288 Oct  5 17:48 gdbSession.txt
-rw------- 1 thonkerpad thonkerpad   7569 Oct  5 17:48 inodes.cpp
-rw-rw-r-- 1 thonkerpad thonkerpad  32224 Oct  5 17:48 inodes.o
-rw------- 1 thonkerpad thonkerpad    722 Oct  5 17:48 Makefile
-rw------- 1 thonkerpad thonkerpad   3641 Oct  5 17:48 mount.cpp
-rw-rw-r-- 1 thonkerpad thonkerpad  30328 Oct  5 17:48 mount.o
-rwxrwxr-x 1 thonkerpad thonkerpad 143888 Oct  5 21:42 P0
-rw-rw-r-- 1 thonkerpad thonkerpad   3850 Oct  5 17:48 read.me
-rw-rw-r-- 1 thonkerpad thonkerpad     35 Oct  5 22:14 ReadMe.txt
-rw------- 1 thonkerpad thonkerpad  12035 Oct  5 21:38 shell.cpp
-rw-rw-r-- 1 thonkerpad thonkerpad  64064 Oct  5 21:42 shell.o
-rw------- 1 thonkerpad thonkerpad   3780 Oct  5 17:48 simdisk.cpp
-rw-rw-r-- 1 thonkerpad thonkerpad  29016 Oct  5 19:01 simdisk.o
-rw-rw-r-- 1 thonkerpad thonkerpad     90 Oct  5 17:48 stdTestScriptP0.txt
-rw-rw-r-- 1 thonkerpad thonkerpad    314 Oct  5 20:40 test.txt
-rw-rw-r-- 1 thonkerpad thonkerpad      0 Oct  5 17:48 textp
-rw------- 1 thonkerpad thonkerpad    112 Oct  5 17:48 user.cpp
-rw------- 1 thonkerpad thonkerpad   6808 Oct  5 17:48 volume.cpp
-rw-rw-r-- 1 thonkerpad thonkerpad  34160 Oct  5 17:48 volume.o

Redirection:
With my project, I was able to implement both Redirection and Background processes. For Redirection I first looked through
the buf in order to determin if there were any special symbols in from the input. If there was then I parse out the name of
the file after the '>' symbol and then change the standard out to be to that file. Now when the command is run it will go 
to the typed file instead. Finially after it has run it will return the standard out to normal.

Piping:
Sadly I was unable to get piping to work but I made quite an attempt to. I understand that a pipe should fork into a 
parent and child process. I attemted to direct the output of the parent process to be the input of the child process
effectivly making the output of the first command typed become the input of the second command typed. I had no issues
parsing out the '|' symbol or any symbol really just getting the piping to actually work.

Background process:
To make a background process I simply forked. After this I had the child process go on to execute the given command
and then had the parent process go to the top of the loop in order to give immedietly give access to the shell. 