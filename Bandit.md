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
####The motive of this level is to access a file called - from the home directory.
 login :ssh bandit1@bandit.labs.overthewire.org -p 2220
        ls to list the files in the cwd.We see a file named - or we use ls -a to view hidden files.
        cat ./- is used to view the file after making it executable.
ls
cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi


## LEVEL 2 --> 3
####The motive of this level is to open a file which has spaces in its name.
login: ssh bandit2@bandit.labs.overthewire.org -p 2220
ls to list the files in the cwd.
cat spaces in this filename with forward slashes before the spaces start.

ls
cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

## LEVEL 3 --> 4
####The motive of this level is to
ls
cd inhere
ls -a
cat .hidden

## LEVEL 0 --> 1
ls
cd inhere
file *
file ./*
cat ./-file07

## LEVEL 0 --> 1
ls
cd inhere
ls
ls -al * | grep -B 10 1033
cat maybehere07/.file2

## LEVEL 0 --> 1
cd ../..
find ./ -group bandit6 -user bandit7 -size 33c
found  ./var/lib/dpkg/info/bandit7.password
cat ./var/lib/dpkg/info/bandit7.password

## LEVEL 0 --> 1
cat data.txt | grep millionth

## LEVEL 0 --> 1
ls
sort data.txt | uniq -u

## LEVEL 0 --> 1
ls
cat data.txt | grep "="
strings data.txt

## LEVEL 0 --> 1
ls
cat data.txt
base64 -d data.txt

## LEVEL 0 --> 1
ls
cat data.txt
used CyberChef cipher to decode ROT13
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)

## LEVEL 0 --> 1
ls
cat data.txt
mkdir /tmp/newfile666
cp data.txt /tmp/new123
cd /tmp/newfile666
xxd -r data.txt data
file data
mv data data.gz
gzip -d data.gz
file data
mv data data.bz2
bzip2 -d data.bz2
file data
mv data data.gz
gzip -d data.gz
file data
tar -x -f data
file data5.bin
tar -x -f data5.bin
file data6.bin
bzip2 -d data6.bin
file data6.bin.out
tar -x -f data6.bin.out
file data8.bin
mv data8.bin data8.gz
gzip -d data8.gz
file data8
cat data



  
 
