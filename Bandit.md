# BANDIT_WARGAME

## LEVEL 0 

#### The motive of this level is to log into the game using an ssh(Basically connecting the game to the terminal using a ssh).<br />
So we use the command:<br /> 
### _ssh bandit0@bandit.labs.overthewire.org -p 2220_<br />
We specify the username@host.server<br />
-p is for specifiying the port.<br />
 
 Learned:<br />
       _Format for using ssh._<br />

## LEVEL 0 --> 1
#### The motive of this level is to access a text file on the server.
 login: ssh bandit0@bandit.labs.overthewire.org -p 2220
        Used the ls command to list the files in the cwd.
        Then we will use cat to see the contents of the file.
ls
cat readme.txt
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL


## LEVEL 1 --> 2
#### The motive of this level is to access a file called - from the home directory.
 login :ssh bandit1@bandit.labs.overthewire.org -p 2220
        ls to list the files in the cwd.We see a file named - or we use ls -a to view hidden files.
        cat ./- is used to view the file after making it executable.
ls
cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi


## LEVEL 2 --> 3
#### The motive of this level is to open a file which has spaces in its name.
login: ssh bandit2@bandit.labs.overthewire.org -p 2220
ls to list the files in the cwd.
cat spaces in this filename with forward slashes before the spaces start.

ls
cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

## LEVEL 3 --> 4
#### The motive of this level is to find a hidden file in the inhere directory.
login: ssh bandit3@bandit.labs.overthewire.org -p 2220
ls (to list the files in the cwd.)
cd (to change the cwd to the inhere directory.)
ls -a (to find the hidden file.)
cat .hidden (where the . specifies that the file is hidden)
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

## LEVEL 4 --> 5
#### The motive of this level is to access the ony human-readable file in the inhere directory.
login: ssh bandit4@bandit.labs.overthewire.org -p 2220
ls to list the files in the cwd. 
cd inhere to change cwd. 
file ./* to exe all(*) the files and find the file type.
We see that only one file is in the ascii text format.
cat ./-file07 to see the password.
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR


## LEVEL 5 --> 6
#### The motive of this level is to access a file with some specific characteristics.
login: ssh bandit5@bandit.labs.overthewire.org -p 2220
ls to list the files in the cwd.
cd inhere to change cwd.
ls to list the files in the cwd.
find -readable -size 1033c ! -executable (to find a readable file with size 1033bytes which is not executable.)
cat maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU


## LEVEL 6 --> 7
#### The motive of this level is to access a file with some specific characteristics.
login: ssh bandit6@bandit.labs.overthewire.org -p 2220
find / -type f -user bandit7 -group bandit6 -size 33c 2> /dev/null (here we specified the characteristics and 2>/dev/null redirects errors to the void)
./var/lib/dpkg/info/bandit7.password
cat ./var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## LEVEL 7 --> 8
#### The motive of this level is to use grep and cat simultaneously.
login: ssh bandit7@bandit.labs.overthewire.org -p 2220
ls to list the files in the cwd.
cat data.txt | grep millionth
####Here what we did was use the piping operator which can redirect the output of one command to the next.
TESKZC0XvTetK0S9xNwm25STk5iWrBvP


## LEVEL 8 --> 9
#### The motive of this level is to find the line that only repeates once.
login: ssh bandit8@bandit.labs.overthewire.org -p 2220
ls
sort data.txt | uniq -u 
 sort command sorts the text in data.txt and after that we use uniq -u here uniq command removes the repeated lines by default while the -u option only retrieves the unique line.
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## LEVEL 9 --> 10
#### The motive of this level is to find the only human-readable strings in the string preceded by many "=". 
login: ssh bandit9@bandit.labs.overthewire.org -p 2220
ls
cat data.txt | strings data.txt | grep "="
Strings command brings out the only readable strings in the file data.txt and grep is used to get the text which is preceded by =.
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s


## LEVEL 10 --> 11
#### The motive of this level is to decode the base64 encrypted text.
login: ssh bandit10@bandit.labs.overthewire.org -p 2220
ls
cat data.txt
base64 -d data.txt 
Here -d option specifies 'Decode'.
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## LEVEL 11 --> 12
#### The motive of this level is to decode a ROT13 cipher encrypted text to obtain the password.
login: ssh bandit11@bandit.labs.overthewire.org -p 2220
ls
cat data.txt
cat random.txt | tr "[a-z][A-Z]" "[n-za-m][N-ZA-M]"
tr short for transilate converts a specified convention to another order)
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## LEVEL 12 --> 13
#### The motive of this level is to create a directory under tmp(a.k.a temporary) and uncompress a multiple time compressed file using various uncompressions.
login: ssh bandit12@bandit.labs.overthewire.org -p 2220
ls
cat data.txt
mkdir /tmp/b4st4rd
cp data.txt /tmp/b4st4rd
xxd -r data.txt > cat file.bin
file file.bin
mv file.bin schnider.gz
gzip -d schnider.gz
ls --> schnider
file schnider
mv schnider schnider.bz
bzip2 -d schnider.bz
file schnider
mv schnider schnider.gz
gzip -d schnider.gz
ls --> schnider
file schnider
mv schnider schnider.tar
tar -xf schnider.tar
ls --> data5.bin
file data5.bin
mv data5.bin schnider.tar
tar -xf schnider.tar
ls --> data6.bin
file data6.bin
mv data6.bin dark_schnider.bz
bzip2 -d dark_schnider.bz
file dark_schnider
mv dark_schnider dark_schnider.tar
tar -xf dark_schnider.tar
ls --> data8.bin
file data.bin 
mv data.bin dark_schnider.gz
gzip -d dark_schnider.gz
file dark_schnider -->dark_schnider ascii text
cat dark_schnider
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw


## LEVEL 13 --> 14
#### The motive of this level is to change user to bandit14 to access a file specifically for bandit14, here u dont have to get the pass but just have to access the bandit14.
login: ssh bandit13@bandit.labs.overthewire.org -p 2220
ls --> sshkey.private
ssh bandit14@localhost -i sshkey.private -p 2220
cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

## LEVEL 14 --> 15
#### The motive of this level is to submit the password of current level to port 30000 of localhost.
login: ssh bandit14@bandit.labs.overthewire.org -p 2220
telnet localhost 30000
Enter the password of the previous level.
Telnet is an application network protocol enables user communication with a remote computer via a text-based interface.
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt


## LEVEL 14 --> 15
#### The motive of this level is to port to 30001 on localhost
openssl s_client -connect localhost:30001
Enter the password of the current level.
JQttfApK4SeyHwDlI9SXGR50qclOAil1



  
 
