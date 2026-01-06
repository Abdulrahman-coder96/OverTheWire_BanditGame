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





\*\*Password:\*\* 263JGJPfgU6LtdEvgfWU1XP5yac29mFx



\*\*What I Learned:\*\*







\# **Level 2 - 3**



\*\*Challenge:\*\*

The password for the next level is stored in a file called 

--spaces in this filename-- located in the home directory.



\*\*Solution:\*\*

Command 1: la -a

Command 2: cat ./"--spaces in this filename--"





\*\*Explanation:\*\*





\*\*Password:\*\* MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx





\*\*What I Learned:\*\*







\# **Level 3 - 4**



\*\*Challenge:\*\*

The password for the next level is stored in a hidden file in the inhere directory.



\*\*Solution:\*\*

**Command 1: ls -la**

**Command 2: cd inhere**

**Command 3: ls -la**

**Command 4: cat ./'...Hiding-From-You'**



\*\*Explanation:\*\*





\*\*Password:\*\* 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ



\*\*What I Learned:\*\*





\# **Level 4 - 5**



\*\*Challenge:\*\*

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cd inhere

Command 3: ls -la

Command 4: cat ./'-file07'





\*\*Explanation:\*\*







\*\*Password:\*\* 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw





\*\*What I Learned:\*\*





\# **Level 5 - 6**



\*\*Challenge:\*\*

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:



* human-readable
* 1033 bytes in size
* not executable





\*\*Solution:\*\*

Command 1: ls -la

Command 2: cd inhere

Command 3: ls -la

Command 4: cd maybehere07

Command 5: ls -la

Command 6: cat ./'.file2'





\*\*Explanation:\*\*





\*\*Password:\*\* HWasnPhtq9AVKe0dmk45nxy20cvUa6EG





\*\*What I Learned:\*\*







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





\*\*Password:\*\* morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj





\*\*What I Learned:\*\*





\# **Level 7 - 8**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt next to the word millionth.





\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: grep millionth data.txt







\*\*Explanation:\*\*





\*\*Password:\*\* dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc





\*\*What I Learned:\*\*





\# **Level 8 - 9**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: sort data.txt | uniq -c | head





\*\*Explanation:\*\*





\*\*Password:\*\* 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM





\*\*What I Learned:\*\*





\# **Level 9 - 10**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt





\*\*Explanation:\*\*





\*\*Password:\*\* FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey





\*\*What I Learned:\*\*





\# **Level 10 - 11**



\*\*Challenge:\*\*

**The password for the next level is stored in the file data.txt, which contains base64 encoded data**





\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: base64 -d data.txt





\*\*Explanation:\*\*





\*\*Password:\* dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr





\*\*What I Learned:\*\*





\# **Level 11 - 12**



\*\*Challenge:\*\*

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.



\*\*Solution:\*\*

Command 1: ls -la

Command 2: cat data.txt

Command 3: cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'





\*\*Explanation:\*\*







\*\*Password:\* 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4





\*\*What I Learned:\*\*





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





\*\*Password:\* FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn





\*\*What I Learned:\*\*





\# **Level 13 - 14**



\*\*Challenge:\*\*

The password for the next level is stored in /etc/bandit\_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.





\*\*Solution:\*\*







\*\*Explanation:\*\*







\*\*Password:\*







\*\*What I Learned:\*\*



