# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![Screenshot from 2024-02-19 16-22-51](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/c35eee39-b77b-42f5-ae91-42caecdd52da)


cat < file2
## OUTPUT
![Screenshot from 2024-02-19 17-28-31](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/682bbd9a-6678-4624-b5f7-6daaf396807c)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2024-02-19 17-32-20](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/8640faa3-8194-4ee4-a16c-dd365e6905ec)

comm file1 file2
 ## OUTPUT
![Screenshot from 2024-02-19 17-35-16](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/71f6a18b-cb96-46ac-b04c-8a90319de369)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-02-19 21-06-13](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/59e72bbd-0260-45a8-b1a4-1b685695971c)



#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![Screenshot from 2024-02-19 21-09-44](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2464b3f4-6b08-41be-aa67-e117fd96dfc1)




cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2024-02-19 21-10-52](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/86de4428-9ee0-485d-9696-cbac521429a0)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-02-19 21-23-06](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/68a6922d-20c0-4af8-921a-d7a14af1d483)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-33-58](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/5225be44-5ded-479f-81c0-1b08a43a3db2)



grep hello newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-35-38](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/78ef312e-f2f6-4d3d-a656-eb5f93641a61)




grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-36-08](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2e1628ca-d122-4a5c-8616-8c6c318f224b)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2024-02-19 21-36-39](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/79b59c5f-d111-43af-a1b8-1cd24831653c)



cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2024-02-19 21-37-05](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/fd5bc91e-6d16-42f4-913b-8baedfae7d67)




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-02-19 21-42-45](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/10e88fba-0b66-41aa-bf4d-1eec3ec8bb73)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-46-41](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2f7618eb-26c9-4a06-b037-6e2a05e035a8)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-49-41](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/1586acca-2c82-4c42-98bc-4ae798eef1a8)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2024-02-19 21-52-25](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/8688c525-73fb-44c1-aedc-42c6bf61741e)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-52-49](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/4980783d-eee0-4468-a932-ed98b32fb05f)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-53-18](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/0c3b9da2-1ec3-4ed6-afdf-d97b3ec65697)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-53-48](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/69094a6a-7169-4233-8e34-b63fd3b50f86)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-54-11](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/228361e3-4c51-408b-acae-b547654c8d92)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-54-38](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/78841f5b-a1d6-42da-a170-f873f2db1c02)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-55-00](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/218b2ba3-76f4-4fe8-8822-3d64fc006de9)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-55-18](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/e0fb9fd4-0e34-4bb0-b447-480e7353e23c)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-02-19 21-55-54](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/455cefd1-c3cf-4a56-9626-22f5acc9d758)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-02-19 21-56-46](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/8b7b973d-2ecb-4adf-b3b0-b4a6090238f4)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![Screenshot from 2024-02-19 22-03-40](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/6ed8eeb2-98aa-489d-b7b5-502fad1fa948)



sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2024-02-19 22-04-04](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/a525b7f6-5451-4607-bf43-47e41df195cc)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2024-02-19 22-04-27](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2dec5d41-9a09-4e5e-8b9e-124614c5ba56)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-19 22-04-47](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/18fb9a8e-d5ce-4f68-8d04-799b2e781cd6)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-02-19 22-05-04](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/5209fed2-c815-4dd9-bbfc-885f9104d28a)



sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2024-02-19 22-05-27](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/59481f62-1000-4099-be96-30a15f0f9f9f)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2024-02-19 22-06-07](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/c1935ffc-35e7-488e-a332-e3dd4c0b4220)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-02-19 22-09-55](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/3156abad-90b0-40bc-82f2-7e288e6776c9)



seq 10 
## OUTPUT

![Screenshot from 2024-02-19 22-10-26](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/ea0f93d4-b7fe-4b56-83f8-5df261f74fcb)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2024-02-19 22-13-29](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/bc5e24b5-5130-4756-b972-bd061802099e)


seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2024-02-19 22-13-48](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/af99d8d5-a0fb-4a3f-8391-4ce396c27f9f)



seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2024-02-19 22-14-24](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/ebff4972-2af6-4823-8af3-5a2218ed0f9e)


seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-02-19 22-14-48](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/6a7d5a34-213f-4d78-a264-72be126d9325)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-02-19 22-15-21](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/56f96442-9167-4513-812b-07e8b22b9252)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2024-02-19 22-15-43](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/cbadd6df-119c-4a6a-b7ac-8888a033311e)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT:
![Screenshot from 2024-02-19 22-16-01](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/36d38ad5-fd86-4e5d-86f3-734e1c0390bc)



#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![Screenshot from 2024-02-19 23-32-00](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/b947d6ba-4de8-436b-a7b7-fd88455c4fa3)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![Screenshot from 2024-02-19 23-33-39](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/df15d132-7d04-43d4-ae87-87bb88a3e002)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-02-19 23-35-40](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2fe37e25-e5ba-4bbb-9209-9980e7b79ff5)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![Screenshot from 2024-02-19 23-38-44](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/3d90c98b-a7b3-43f6-8674-b310a5ab193b)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2024-02-19 23-40-24](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/ca555058-30ad-4a25-899a-81179c28d117)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-02-24 10-23-11](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/d813cb49-6684-4e3c-8570-ea7d6368b688)

![Screenshot from 2024-02-24 10-23-40](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/70216941-d36d-4b4a-88a5-8243e9fd3ebf)

tar -xvf backup.tar
## OUTPUT
![alt text](image-43.png)

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
![alt text](image-44.png)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![alt text](image-49.png)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![alt text](image-50.png)

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![alt text](image-51.png)
 
ls file1
## OUTPUT
![alt text](image-52.png)
echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![alt text](image-53.png)
abcd
 
echo $?
 ## OUTPUT
![alt text](image-54.png)

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
![alt text](image-55.png)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![alt text](image-56.png)

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![alt text](image-57.png)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![alt text](image-58.png)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![alt text](image-59.png)
# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![alt text](image-60.png)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![alt text](image-61.png)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![alt text](image-62.png)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 

![alt text](image-63.png)
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
![alt text](image-64.png)
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 ![alt text](image-65.png)
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 ![alt text](image-66.png)
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
![alt text](image-67.png)
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
![alt text](image-68.png)
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![alt text](image-69.png)

cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![alt text](image-70.png)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![alt text](image-71.png)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![alt text](image-72.png)
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![alt text](image-73.png)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
![alt text](image-74.png)
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![alt text](image-75.png)
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![alt text](image-76.png)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![alt text](image-77.png)


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
![alt text](image-78.png)
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
![alt text](image-79.png)
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
![alt text](image-80.png)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
![alt text](image-83.png)
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
![alt text](image-82.png)
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![alt text](image-84.png)

# RESULT:
The Commands are executed successfully.
