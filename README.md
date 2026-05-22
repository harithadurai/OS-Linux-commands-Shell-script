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

<img width="727" height="173" alt="image" src="https://github.com/user-attachments/assets/4a165bc9-52a4-4284-98bc-de0cf552dd98" />


cat < file2
## OUTPUT

<img width="657" height="225" alt="image" src="https://github.com/user-attachments/assets/a9660b26-62c0-4436-bb07-899aa91c70a3" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="420" height="68" alt="image" src="https://github.com/user-attachments/assets/0788f95b-1707-481f-b34e-e4754f1bcc27" />

 
comm file1 file2
 ## OUTPUT

 
<img width="399" height="209" alt="Screenshot 2026-05-16 203028" src="https://github.com/user-attachments/assets/e54058e5-e1e9-4896-8a1a-335c892197a1" />

 
diff file1 file2
## OUTPUT

<img width="338" height="284" alt="Screenshot 2026-05-16 203150" src="https://github.com/user-attachments/assets/24ff4c32-4d0a-445d-b841-d7ed315e52c5" />


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

<img width="403" height="97" alt="image" src="https://github.com/user-attachments/assets/92c8cc73-18a4-4b6f-acde-435495e06e0b" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="353" height="152" alt="image" src="https://github.com/user-attachments/assets/5a57ab79-3540-46be-ab7c-d2be4b3c4fa4" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="487" height="150" alt="image" src="https://github.com/user-attachments/assets/78b40ee7-8330-4d6d-a9dc-40e44be97783" />



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

<img width="362" height="91" alt="image" src="https://github.com/user-attachments/assets/b449a468-96f5-490c-91fc-ea9c28b686f3" />



grep hello newfile 
## OUTPUT

<img width="426" height="80" alt="image" src="https://github.com/user-attachments/assets/0d288c9c-125c-41fc-96d8-19197093485e" />


grep -v hello newfile 
## OUTPUT

<img width="452" height="108" alt="image" src="https://github.com/user-attachments/assets/dc806a25-35f9-4660-8af7-68c51ef6c736" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="417" height="105" alt="image" src="https://github.com/user-attachments/assets/9c483408-fe77-4a58-b2d4-d45fa0eed316" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="468" height="86" alt="image" src="https://github.com/user-attachments/assets/9a8d78c5-dc31-4ae7-8d29-35748f9b2953" />



grep -R ubuntu /etc
## OUTPUT

<img width="802" height="331" alt="image" src="https://github.com/user-attachments/assets/a38c18d0-50e3-429b-9e6b-c5028d04b6c9" />


grep -w -n world newfile   
## OUTPUT

<img width="397" height="101" alt="image" src="https://github.com/user-attachments/assets/5cd56193-a21a-4e61-9f73-803dd1cc6360" />


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

<img width="518" height="106" alt="image" src="https://github.com/user-attachments/assets/1f735b58-4e20-4b0e-b410-08ebd2416a39" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="481" height="86" alt="image" src="https://github.com/user-attachments/assets/bcd93915-7e74-44d8-bacd-9ee7f4d0ad01" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="507" height="91" alt="image" src="https://github.com/user-attachments/assets/8488eb63-5325-4ca6-9707-2a874ff2b25e" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="523" height="72" alt="image" src="https://github.com/user-attachments/assets/a487f1da-eb59-45a6-a57f-ede71736df0c" />


egrep '(world$)' newfile 
## OUTPUT

<img width="590" height="100" alt="image" src="https://github.com/user-attachments/assets/95e4bbd1-bdb8-467c-95ce-a48423bff8d3" />


egrep '(World$)' newfile 
## OUTPUT

<img width="606" height="87" alt="image" src="https://github.com/user-attachments/assets/4ad62313-db70-41d0-947b-67f7f54815b1" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="597" height="112" alt="image" src="https://github.com/user-attachments/assets/f20126f3-d889-4cdc-a222-d26bee423bfa" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="567" height="87" alt="image" src="https://github.com/user-attachments/assets/3ed4656c-34e6-4a6e-90cf-d8b2061ee87e" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="422" height="92" alt="image" src="https://github.com/user-attachments/assets/9d9e9e52-4e8d-43d4-8801-87b927e85571" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="460" height="77" alt="image" src="https://github.com/user-attachments/assets/2c15a393-2f71-4a5d-a39d-7a892a0fc4a8" />


egrep l{2} newfile
## OUTPUT

<img width="373" height="112" alt="image" src="https://github.com/user-attachments/assets/683da0a3-a9f3-4787-b967-833566c2bf14" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="403" height="118" alt="image" src="https://github.com/user-attachments/assets/4003f808-b120-406f-bcb4-256e212fb6a2" />


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

<img width="343" height="77" alt="image" src="https://github.com/user-attachments/assets/0b54fa4e-56b1-4174-b5d6-3fa976f76eff" />


sed -n -e '$p' file23
## OUTPUT

<img width="457" height="80" alt="image" src="https://github.com/user-attachments/assets/62f4faf3-35a3-4be7-87b4-5ef1f762d5a3" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="600" height="275" alt="image" src="https://github.com/user-attachments/assets/10759768-503b-45dd-b152-6e7bab0d5439" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="492" height="281" alt="image" src="https://github.com/user-attachments/assets/91aaa02c-5511-4cfe-8150-571ec8066ae6" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="532" height="267" alt="image" src="https://github.com/user-attachments/assets/d960964e-243d-42b1-837d-ff5c66b925f0" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="412" height="188" alt="image" src="https://github.com/user-attachments/assets/c28fc965-7a3b-4f26-8f69-43ffd965be12" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="511" height="132" alt="image" src="https://github.com/user-attachments/assets/d99f2275-877c-4943-ab67-9024c5b735cc" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="522" height="118" alt="image" src="https://github.com/user-attachments/assets/a1c78306-4461-455f-8f98-8fae25881956" />


seq 10 
## OUTPUT

<img width="453" height="305" alt="image" src="https://github.com/user-attachments/assets/a2134a4f-eb42-4c81-91a1-f8bfd00aa186" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="405" height="127" alt="image" src="https://github.com/user-attachments/assets/6380f6ea-f773-4263-a824-354485b0650b" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="443" height="123" alt="image" src="https://github.com/user-attachments/assets/30af3c0a-5135-435c-8000-f9831ac50af7" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="453" height="158" alt="image" src="https://github.com/user-attachments/assets/4f94bca8-b68d-462e-86b9-8bb26a5efbde" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="522" height="145" alt="image" src="https://github.com/user-attachments/assets/21e86531-70ab-4cb5-b37c-d7bc849383d0" />


seq 10 | sed '2,9c hello'
## OUTPUT


<img width="461" height="125" alt="image" src="https://github.com/user-attachments/assets/49a7b812-a633-464a-b221-3a0740dd7b8a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="512" height="135" alt="image" src="https://github.com/user-attachments/assets/0c3e4625-f564-44fc-aabd-5819d24f7e76" />


sed -n '2,4{s/$/*/;p}' file23


<img width="587" height="135" alt="image" src="https://github.com/user-attachments/assets/2d268c30-0f33-4781-800a-528c2b37a843" />


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

<img width="477" height="182" alt="image" src="https://github.com/user-attachments/assets/67f04287-d043-4fca-89dd-1788b096990d" />


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

<img width="367" height="186" alt="image" src="https://github.com/user-attachments/assets/e5bcfc53-1dee-4b5b-b91f-73680f89f67d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="497" height="278" alt="image" src="https://github.com/user-attachments/assets/79e3e8d1-e5f0-45f5-bf8b-713aed20ccc8" />


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

<img width="437" height="157" alt="image" src="https://github.com/user-attachments/assets/9f667a02-a48f-4f3b-98bc-94abc4be8098" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="513" height="160" alt="image" src="https://github.com/user-attachments/assets/4a781eaf-c6dd-4616-b2eb-11820dd7c3b2" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="791" height="582" alt="Screenshot 2026-05-21 203126" src="https://github.com/user-attachments/assets/6cbbf290-0777-48b4-be96-b84f61f2d051" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="789" height="608" alt="Screenshot 2026-05-21 203440" src="https://github.com/user-attachments/assets/7b976f99-faf1-4de8-ae35-ec5a4c6e0769" />


tar -xvf backup.tar
## OUTPUT


<img width="799" height="604" alt="Screenshot 2026-05-21 203655" src="https://github.com/user-attachments/assets/a60c44dd-2900-4509-b598-59cad132064b" />


gzip backup.tar

ls .gz
## OUTPUT


<img width="512" height="309" alt="Screenshot 2026-05-21 204549" src="https://github.com/user-attachments/assets/9a15a99b-b863-4330-9f4c-0b7fd95a2a33" />

 
gunzip backup.tar.gz
## OUTPUT


<img width="512" height="309" alt="Screenshot 2026-05-21 204549" src="https://github.com/user-attachments/assets/75d7573f-ffd9-4ad4-ab39-4708c78463e4" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="803" height="160" alt="image" src="https://github.com/user-attachments/assets/f0f0599f-9c5c-4568-8f56-62c6da4d4dd5" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="410" height="157" alt="image" src="https://github.com/user-attachments/assets/1738bdb8-83cf-4b89-8586-6abf8802c11f" />

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
 <img width="438" height="328" alt="image" src="https://github.com/user-attachments/assets/207fdcab-0cd6-4004-a582-78ebc1a3c1ed" />

chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="737" height="435" alt="image" src="https://github.com/user-attachments/assets/4d595a82-20a0-4a94-8c76-c8194266feed" />

 
ls file1
## OUTPUT

<img width="452" height="157" alt="image" src="https://github.com/user-attachments/assets/4a56d78b-d557-426f-aa14-37311f53f74d" />


echo $?
## OUTPUT 

<img width="338" height="73" alt="image" src="https://github.com/user-attachments/assets/9357aa01-0bdd-4b1b-b93a-84326e02042f" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="398" height="85" alt="image" src="https://github.com/user-attachments/assets/343bd09c-ccba-41ba-8c2a-19444ea5cc3c" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="398" height="85" alt="image" src="https://github.com/user-attachments/assets/5057525e-36ec-47f6-b49c-fc4fea11ceb5" />


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

<img width="445" height="285" alt="image" src="https://github.com/user-attachments/assets/efae2b25-2ae4-4196-90a6-de6fd9632e41" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="717" height="153" alt="image" src="https://github.com/user-attachments/assets/8cdd7e3f-d10c-4b18-8129-df693ccf4ffd" />



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

<img width="793" height="85" alt="image" src="https://github.com/user-attachments/assets/9471b71f-d623-404b-af48-a601692ca31d" />


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

<img width="622" height="562" alt="image" src="https://github.com/user-attachments/assets/1b850692-ed1c-4bbe-967a-fab1c5374198" />


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

<img width="682" height="158" alt="image" src="https://github.com/user-attachments/assets/23230ac2-cdb3-4e4a-823c-064b0876da63" />


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

<img width="785" height="187" alt="image" src="https://github.com/user-attachments/assets/5d71ca9b-ae0b-4779-afe5-6e84ffc80930" />


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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.
