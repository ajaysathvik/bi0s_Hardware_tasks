# BANDIT_WARGAME

## LEVEL 0 

#### The motive of this level is to log into the game using an ssh(Basically connecting the game to the terminal using a ssh).<br />
So we use the command:<br /> 
### _ssh bandit0@bandit.labs.overthewire.org -p 2220_<br />
We specify the username@host.server<br />
-p is for specifiying the port.<br />
 
 #### Learned:<br />
              Format for using ssh.

## LEVEL 0 --> 1
#### The motive of this level is to access a text file on the server.<br />
 login: <br />
       ssh bandit0@bandit.labs.overthewire.org -p 2220<br />
        Used the ls command to list the files in the cwd.
        Then we will use cat to see the contents of the file.
ls<br />
cat readme.txt<br />
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL<br />

#### Learned:<br />
     ls , cat commands.


## LEVEL 1 --> 2
#### The motive of this level is to access a file called - from the home directory.<br />
 login :<br />
 ssh bandit1@bandit.labs.overthewire.org -p 2220<br />
        ls to list the files in the cwd.We see a file named - or we use ls -a to view hidden files.<br />
        cat ./- is used to view the file after making it executable.<br />
ls<br />
cat ./-<br />
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi<br />

#### Learned:<br />
     ./ command executes the file

## LEVEL 2 --> 3
#### The motive of this level is to open a file which has spaces in its name.<br />
login: 
ssh bandit2@bandit.labs.overthewire.org -p 2220<br />
ls to list the files in the cwd.<br />
cat spaces in this filename with forward slashes before the spaces start.<br />

ls<br />
cat spaces\ in\ this\ filename<br />
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG<br />

#### Learned:<br />
     Forward slashes before a space in a filename with spaces can void the error while using the file.

## LEVEL 3 --> 4
#### The motive of this level is to find a hidden file in the inhere directory.
login: ssh bandit3@bandit.labs.overthewire.org -p 2220<br />
ls (to list the files in the cwd.)<br />
cd (to change the cwd to the inhere directory.)<br />
ls -a (to find the hidden file.)<br />
cat .hidden (where the . specifies that the file is hidden)<br />
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe<br />

#### Learned:<br />
     How to view and open a hidden file.

## LEVEL 4 --> 5
#### The motive of this level is to access the ony human-readable file in the inhere directory.
login: ssh bandit4@bandit.labs.overthewire.org -p 2220<br />
ls to list the files in the cwd. <br />
cd inhere to change cwd. <br />
file ./* to exe all(*) the files and find the file type.<br />
We see that only one file is in the ascii text format.<br />
cat ./-file07 to see the password.<br />
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR<br />

#### Learned:<br />
      Working of file command.
      Astar key is used to select all.

## LEVEL 5 --> 6
#### The motive of this level is to access a file with some specific characteristics.
login: ssh bandit5@bandit.labs.overthewire.org -p 2220<br />
ls to list the files in the cwd.<br />
cd inhere to change cwd.<br />
ls to list the files in the cwd.<br />
find -readable -size 1033c ! -executable (to find a readable file with size 1033bytes which is not executable.)<br />
cat maybehere07/.file2<br />
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU<br />

#### Learned:<br />
     Find command use.
     How to find a specific file.

## LEVEL 6 --> 7
#### The motive of this level is to access a file with some specific characteristics.
login: ssh bandit6@bandit.labs.overthewire.org -p 2220<br />
find / -type f -user bandit7 -group bandit6 -size 33c 2> /dev/null (here we specified the characteristics and 2>/dev/null redirects errors to the void)<br />
./var/lib/dpkg/info/bandit7.password<br />
cat ./var/lib/dpkg/info/bandit7.password<br />
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S<br />

#### Learned:<br />
     How to find a specific file.

## LEVEL 7 --> 8
#### The motive of this level is to use grep and cat simultaneously.
login: ssh bandit7@bandit.labs.overthewire.org -p 2220<br />
ls to list the files in the cwd.<br />
cat data.txt | grep millionth<br />
####Here what we did was use the piping operator which can redirect the output of one command to the next.<br /><br />
TESKZC0XvTetK0S9xNwm25STk5iWrBvP<br />

#### Learned:<br />
     grep command  and piping.

## LEVEL 8 --> 9
#### The motive of this level is to find the line that only repeates once.
login: ssh bandit8@bandit.labs.overthewire.org -p 2220<br />
ls<br />
sort data.txt | uniq -u <br />
 sort command sorts the text in data.txt and after that we use uniq -u here uniq command removes the repeated lines by default while the -u option only retrieves the unique line.<br />
EN632PlfYiZbn3PhVK3XOGSlNInNE00t<br />

#### earned:<br />
     sort command to sort the file.
     uniq -u command to get a unique non-reccuring line of text.

## LEVEL 9 --> 10
#### The motive of this level is to find the only human-readable strings in the string preceded by many "=". 
login: ssh bandit9@bandit.labs.overthewire.org -p 2220<br />
ls<br />
cat data.txt | strings data.txt | grep "="<br />
Strings command brings out the only readable strings in the file data.txt and grep is used to get the text which is preceded by =.<br />
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s<br />

#### Learned:<br />
     More piping.
     String command useage.

## LEVEL 10 --> 11
#### The motive of this level is to decode the base64 encrypted text.
login: ssh bandit10@bandit.labs.overthewire.org -p 2220<br />
ls<br />
cat data.txt<br />
base64 -d data.txt <br />
Here -d option specifies 'Decode'.<br />
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM<br />

#### Learned:<br />
     How to decode base64 encryption using linux terminal.

## LEVEL 11 --> 12
#### The motive of this level is to decode a ROT13 cipher encrypted text to obtain the password.
login:
ssh bandit11@bandit.labs.overthewire.org -p 2220<br />
ls<br />
cat data.txt<br />
cat random.txt | tr "[a-z][A-Z]" "[n-za-m][N-ZA-M]"<br />
tr short for transilate converts a specified convention to another order)<br />
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv<br />

#### Learned:<br />
     tr or translate commands usage.

## LEVEL 12 --> 13
#### The motive of this level is to create a directory under tmp(a.k.a temporary) and uncompress a multiple time compressed file using various uncompressions.
login: ssh bandit12@bandit.labs.overthewire.org -p 2220<br />
ls<br />
cat data.txt<br />
mkdir /tmp/b4st4rd<br />
cp data.txt /tmp/b4st4rd<br />
xxd -r data.txt > cat file.bin<br />
file file.bin<br />
mv file.bin schnider.gz<br />
gzip -d schnider.gz<br />
ls --> schnider<br />
file schnider<br />
mv schnider schnider.bz<br />
bzip2 -d schnider.bz<br />
file schnider<br />
mv schnider schnider.gz<br />
gzip -d schnider.gz<br />
ls --> schnider<br />
file schnider<br />
mv schnider schnider.tar<br />
tar -xf schnider.tar<br />
ls --> data5.bin<br />
file data5.bin<br />
mv data5.bin schnider.tar<br />
tar -xf schnider.tar<br />
ls --> data6.bin<br />
file data6.bin<br />
mv data6.bin dark_schnider.bz<br />
bzip2 -d dark_schnider.bz<br />
file dark_schnider<br />
mv dark_schnider dark_schnider.tar<br />
tar -xf dark_schnider.tar<br />
ls --> data8.bin<br />
file data.bin <br />
mv data.bin dark_schnider.gz<br />
gzip -d dark_schnider.gz<br />
file dark_schnider -->dark_schnider ascii text<br />
cat dark_schnider<br />
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw<br />

#### Learned:<br />
    xxd -r command to covert a hexadump file to bin file.
    How to uncompress different types of files.


## LEVEL 13 --> 14
#### The motive of this level is to change user to bandit14 to access a file specifically for bandit14, here u dont have to get the pass but just have to access the bandit14.
login: ssh bandit13@bandit.labs.overthewire.org -p 2220<br />
ls --> sshkey.private<br />
ssh bandit14@localhost -i sshkey.private -p 2220<br />
cat /etc/bandit_pass/bandit14<br />
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq<br />

#### Learned:<br />
    How to port to a server while in another server using ssh.
    It requires the rsa encrypted private key of the other server.

## LEVEL 14 --> 15
#### The motive of this level is to submit the password of current level to port 30000 of localhost.
login: ssh bandit14@bandit.labs.overthewire.org -p 2220<br />
telnet localhost 30000<br />
Enter the password of the previous level.<br />
Telnet is an application network protocol enables user communication with a remote computer via a text-based interface.<br />
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt<br />

#### Learned:<br />
    Telnet command.

## LEVEL 14 --> 15
#### The motive of this level is to port to 30001 on localhost
openssl s_client -connect localhost:30001<br />
Enter the password of the current level.<br /><br />
JQttfApK4SeyHwDlI9SXGR50qclOAil1<br />

#### Learned:<br />
     openssl , s_client commands on terminal.



  
 
