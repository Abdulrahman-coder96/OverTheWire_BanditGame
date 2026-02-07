**# Level 0** 



\*\*Challenge:\*\* 

Host: bandit.labs.overthewire.org, on port 2220.

Username: bandit0 

Password: bandit0



\*\*Solution:\*\*

ssh bandit0@bandit.labs.overthewire.org -p 2220

Password: bandit0





\*\*Explanation:\*\*

Goal: In this level I had to log into the game using SSH, with a given username, password, host and port.





**# Level 0 - 1**



\*\*Challenge:\*\*

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH.



\*\*Solution:\*\*

Command 1: ls

Command 2: cat readme



\*\*Explanation:\*\*

The command 'ls' lists the files in the working directory. It revealed the file 'readme' which contains the password. I then read the contents of that file using the command 'cat'. This then had the password I was looking for.



\*\*Password:\*\* ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If



\*\*What I Learned:\*\* 

The 'cat' command is incredibly powerful for reading the contents of files and displaying file contents on the terminal.



\# **Level 1 - 2**



\*\*Challenge:\*\*

The password for the next level is stored in a file called - located in the home directory.



\*\*Solution:\*\*

Command 1: ls -a

command 2: cat ./- 



\*\*Explanation:\*\*

The Command ls -a lists all the files and directories stored within the current directory. Then once I've seen the - file then i read the file useing the cat ./- command to get the password stored inside.  



\*\*Password:\*\* 263JGJPfgU6LtdEvgfWU1XP5yac29mFx



\*\*What I Learned:\*\*
Use this Cat ./-  command like this to read files that have names with dashes similar to - this which will not allow you to execute the read command the regular way.





\# **Level 2 - 3**



\*\*Challenge:\*\*

The password for the next level is stored in a file called 

--spaces in this filename-- located in the home directory.



\*\*Solution:\*\*

Command 1: ls -a

Command 2: cat ./"--spaces in this filename--"




\*\*Explanation:\*\*
The Command ls -a lists all the files and directories stored within the current directory. Then once I've seen the --spaces in this filename--  file then i read the file useing the cat ./"--spaces in this filename--" command to get the password stored inside.  





\*\*Password:\*\* MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx





\# **Level 3 - 4**



\*\*Challenge:\*\*

The password for the next level is stored in a hidden file in the inhere directory.



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cd inhere

Command 3: ls -la

Command 4: cat ./'...Hiding-From-You'



\*\*Explanation:\*\*
The Command ls -la lists all the files and directories stored within the current directory. Then once I've seen the inhere directory i use the cd inhere to change into this directory. Then i use the ls -la Command that lists all the files and directories stored within the current directory again. Then I've found the suspected file that may contain the password. I then read the file useing the cat ./'...Hiding-From-You'  command to get the password stored inside.  



\*\*Password:\*\* 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ



\*\*What I Learned:\*\*
I learnt that you have to be careful of not missing spaces or quotation marks as the command may not work without them. Also the ls -la command not only shows files and directories but the level of permission and user etc.




\# **Level 4 - 5**



\*\*Challenge:\*\*

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cd inhere

Command 3: ls -la

Command 4: cat ./'-file07'



\*\*Explanation:\*\*
The Command ls -la lists all the files and directories stored within the current directory. Then once I've seen the inhere directory i use the cd inhere to change into this directory. Then i use the command ls -la to list all the files and directories stored within the current directory again. Once i did this a lot of files popped up and i had to read each one untill I came across the file with the password. This is the command and the file cat ./'-file07'.  




\*\*Password:\*\* 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw




\# **Level 5 - 6**



\*\*Challenge:\*\*

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:



* human-readable
* 1033 bytes in size
* not executable




\*\*Solution:\*\*

Command 1: ls -la

Command 2: cd inhere

Command 3: find . -type f -size 1033c

Command 4: cat ./maybehere07/.file2




\*\*Explanation:\*\*
The Command ls -la lists all the files and directories stored within the current directory. Then change into the inhere directory using the cd inhere command. Then use the ls -la command to list all the files and directories stored within the inhere directory. I then use the find command with the values in the challenge to find the path of the wanted file. I then got the path and i used that cat command to read the file for the password. The command i used was cat ./maybehere07/.file2



\*\*Password:\*\* HWasnPhtq9AVKe0dmk45nxy20cvUa6EG





\*\*What I Learned:\*\*
I found out that the find command is a simple and effective way to find the file path if you have the correct values as it takes you straight to the file your looking for as well as the file path.





\# **Level 6 - 7**



\*\*Challenge:\*\*

The password for the next level is stored somewhere on the server and has all of the following properties:



* owned by user bandit7
* owned by group bandit6
* 33 bytes in size



\*\*Solution:\*\*

Command 1: ls -la 

Command 2: find / -user bandit7 -group bandit6 -size 33c

Command 3: cat /var/lib/dpkg/info/bandit7.password



\*\*Explanation:\*\*

I used the command ls -la to list all the files and directories stored within the current directory. I then used the find command to locate the file path using the given properties given in the challenge. The command i used find / -user bandit7 -group bandit6 -size 33c . I then used the cat command to read the file that contains the password. This is the command i used cat /var/lib/dpkg/info/bandit7.password




\*\*Password:\*\* morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj




\# **Level 7 - 8**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt next to the word millionth.





\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: grep millionth data.txt





\*\*Explanation:\*\*
I used the command ls -la to list all the files and directories stored within the current directory. Once i saw the data.txt i read it using the cat command cat data.txt. I then used the grep command grep millionth data.txt to get the password from the data.txt file which is next to the word millionth.




\*\*Password:\*\* dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc





\*\*What I Learned:\*\*
grep is the tool useed to search for certain word within a file full of words.



\# **Level 8 - 9**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: sort data.txt | uniq -c | head




\*\*Explanation:\*\*
I used the command ls -la to list all the files and directories stored within the current directory. Then when i found the data.txt file i used the cat command to read the file cat data.txt. Then i used the following Sort command sort data.txt | uniq -c | head to sort the files contents by grouping together identical lines, to give a number for occuraces of each line and to give me the top ten lines as that is were the passwrod is within the file. I used pipe inbetween the commands so takes the sorted output and sends it directly to the next command.




\*\*Password:\*\* 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM





\*\*What I Learned:\*\*
Pipe is the | inbetween the commands which takes the sorted output and sends it directly to the next command.




\# **Level 9 - 10**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt





\*\*Explanation:\*\*
I used the command ls -la to list all the files and directories stored within the current directory. I then read the data.txt file with the cat data.txt command. I then scrooled down till i saw several = charaters which had the password right beside it.




\*\*Password:\*\* FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey





\# **Level 10 - 11**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt, which contains base64 encoded data





\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: base64 -d data.txt





\*\*Explanation:\*\*
I used the command ls -la to list all the files and directories stored within the current directory. I then read the data.txt file with the cat data.txt command. Then i used the base64 command with the -d flag to decode. 




\*\*Password:\* dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr





\*\*What I Learned:\*\*
The - d flag used when using the base64 command decodes the data instead on encode it.



\# **Level 11 - 12**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'





\*\*Explanation:\*\*
I used the command ls -la to list all the files and directories stored within the current directory. I then read the data.txt file with the cat data.txt command. Then i read the file with the cat command and then pipe in the second command to execute right after. This is includes tr which to delete and translate characters. This 'A-Za-z' 'N-ZA-Mn-za-m' defines the targeted set. The full command cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' i put together to execute both commmands one after the other got me the password.






\*\*Password:\* 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4





\# **Level 12 - 13**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv





\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: mkdir /tmp/lvl12

Command 4: cp data.txt /tmp/lvl12

Command 5: cd /tmp/lvl12

Command 6: ls -la

Command 7: xxd -r data.txt > data

Command 8: ls

Command 9: file data 

Command 10: mv data file.gz

Command 11: ls 

Command 12: gzip -d file.gz

Command 13: ls

Command 14: file file

Command 15: mv file file.bz2

Command 16: bzip2 -d file.bz2

Command 17: ls

Command 18: bzip2 -d file.bz2

Command 19: ls 

Command 20: file file

Command 21: mv file file.gz

Command 22: ls

Command 23: file file

Command 24: mv file file.tar

Command 25: tar xf file.tar 

Command 26: ls

Command 27: file data5.bin

Command 28: rm file.tar

Command 29: rm data.txt

Command 30: ls

Command 31: file data5.bin

Command 32: mv data5.bin data.tar

Command 33: tar xf data.tar

Command 34: ls

Command 35: file data6.bin 

Command 36: rm data.tar 

Command 37: ls 

Command 38: mv data6.bin data.bz2

Command 39: ls

Command 40: bzip2 -d data.bz2

Command 41: ls

Command 42: file data

Command 43: mv data data.tar

Command 44: ls

Command 45: tar xf data.tar

Command 46: ls

Command 47: file data8.bin

Command 48: rm data.tar

Command 49: mv data8.bin data.gz

Command 50: ls

Command 51: gzip -d data.gz

Command 52: ls

Command 53: file data

Command 54: cat data





\*\*Explanation:\*\*
I used the command ls -la to list all the files and directories stored within the current directory. I then used the cat command to read the data.txt file. Then i make a temporary to work in mkdir /tmp/lvl12. I then copy and paste the data.txt into the the new temporary directory and the cd into that directory. I then used the xxd to turn the text hex dump back into a binary file and reverse the hex dump. Then i repeatedly check the file type and decompress appropriately and keep running file on the resulting output until it finally says "ASCII text", after that i found the password using the cat command.


\*\*Password:\* FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn




\*\*What I Learned:\*\*





\# **Level 13 - 14**



\*\*Challenge:\*\*

The password for the next level is stored in /etc/bandit\_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.





\*\*Solution:\*\*







\*\*Explanation:\*\*







\*\*Password:\*







\*\*What I Learned:\*\*






