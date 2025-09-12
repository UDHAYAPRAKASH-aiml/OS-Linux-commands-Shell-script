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


<img width="409" height="124" alt="image" src="https://github.com/user-attachments/assets/02db877a-a9dd-4f22-bd75-1b33e4aa1c43" />


cat < file2
## OUTPUT
<img width="429" height="97" alt="image" src="https://github.com/user-attachments/assets/d36a5b22-81f4-4269-83d2-d4940547f09d" />


cmp file1 file2
## OUTPUT
 <img width="441" height="31" alt="image" src="https://github.com/user-attachments/assets/703a5f78-3587-41df-8cb1-ffac7c45d418" />

comm file1 file2
 ## OUTPUT
<img width="452" height="101" alt="image" src="https://github.com/user-attachments/assets/691093dc-07db-414a-8038-866fa836d22d" />


 
diff file1 file2
## OUTPUT

<img width="478" height="171" alt="image" src="https://github.com/user-attachments/assets/d50f324d-7e79-4a80-b600-3130b39aafae" />

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


<img width="472" height="58" alt="image" src="https://github.com/user-attachments/assets/fb5a5e1c-a94d-4fcc-a9ef-249515f9a7e5" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="544" height="83" alt="image" src="https://github.com/user-attachments/assets/26b0772f-791f-473d-88b6-6746627d9b4a" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="534" height="74" alt="image" src="https://github.com/user-attachments/assets/30c59a11-276b-4acf-a6d6-c73d6c185e94" />

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

<img width="475" height="33" alt="image" src="https://github.com/user-attachments/assets/c0ae6397-d896-4722-ba8d-791d72f317ab" />



grep hello newfile 
## OUTPUT

<img width="475" height="34" alt="image" src="https://github.com/user-attachments/assets/e19f3f2a-1b8d-43ef-bbff-1cebac09e8bd" />



grep -v hello newfile 
## OUTPUT

<img width="534" height="42" alt="image" src="https://github.com/user-attachments/assets/752e2ee6-54ed-4a36-98d8-325aaf9c3248" />



cat newfile | grep -i "hello"
## OUTPUT



<img width="564" height="42" alt="image" src="https://github.com/user-attachments/assets/b98f3f11-4ad0-4d70-9d87-3555c2cca0cd" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="594" height="43" alt="image" src="https://github.com/user-attachments/assets/e4d3c080-ac15-45f2-ad36-051dd6d4b83f" />



grep -R ubuntu /etc
## OUTPUT

<img width="1041" height="144" alt="image" src="https://github.com/user-attachments/assets/acdc2dc8-1bce-463e-bd5f-d35647445e06" />
<img width="1116" height="333" alt="image" src="https://github.com/user-attachments/assets/4d5daf1a-00b0-4fd7-b8e1-ed64aa18fefc" />



grep -w -n world newfile   
## OUTPUT

<img width="601" height="42" alt="image" src="https://github.com/user-attachments/assets/6a05bc4c-bc3d-4095-9772-dee077f4380b" />

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

<img width="601" height="42" alt="image" src="https://github.com/user-attachments/assets/205c6a5d-2dc3-4d82-a4b4-edd5ff380891" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="601" height="46" alt="image" src="https://github.com/user-attachments/assets/8293f091-9bf7-4621-bd06-87251a170196" />





egrep '(^hello)' newfile 
## OUTPUT

<img width="524" height="39" alt="image" src="https://github.com/user-attachments/assets/0e04cc12-9916-45d2-9dbc-3b7eb96deea4" />


egrep '(world$)' newfile 
## OUTPUT

 <img width="524" height="41" alt="image" src="https://github.com/user-attachments/assets/72db0edb-f752-429c-a3f2-22caab827813" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="714" height="49" alt="image" src="https://github.com/user-attachments/assets/00d1defc-a4cb-4271-b7be-ecdc8bfb56ef" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="500" height="35" alt="image" src="https://github.com/user-attachments/assets/e5d42e28-d950-4256-bede-14c4b9bf70ca" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="552" height="39" alt="image" src="https://github.com/user-attachments/assets/f51127ba-74f4-423d-8489-0cd688d00d5c" />


egrep l{2} newfile
## OUTPUT

<img width="552" height="42" alt="image" src="https://github.com/user-attachments/assets/cbf51958-2042-45ce-9974-e55d6d332ca8" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="552" height="64" alt="image" src="https://github.com/user-attachments/assets/1bd31d34-7177-49cd-87f4-51c420db7fe2" />


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

<img width="511" height="143" alt="Screenshot 2025-09-07 085740" src="https://github.com/user-attachments/assets/3d6732a5-b965-4534-b4ef-2b391d8f0334" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="478" height="327" alt="Screenshot 2025-09-07 085839" src="https://github.com/user-attachments/assets/7e5afab8-bf9a-4190-9f4f-2ea1cbb9fc85" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="492" height="317" alt="Screenshot 2025-09-07 085944" src="https://github.com/user-attachments/assets/3b557937-4d27-49ff-9db9-9dacb524eeae" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="483" height="252" alt="Screenshot 2025-09-07 090007" src="https://github.com/user-attachments/assets/ec2d873b-59fb-4589-9104-f1f419d76f1b" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="584" height="170" alt="Screenshot 2025-09-07 090039" src="https://github.com/user-attachments/assets/563e6e4a-272c-4297-8674-e3030adf1455" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="584" height="170" alt="Screenshot 2025-09-07 090039" src="https://github.com/user-attachments/assets/8cd34497-6432-4ee2-95db-e6673e0253e4" />

seq 10 
## OUTPUT

<img width="609" height="368" alt="Screenshot 2025-09-07 090059" src="https://github.com/user-attachments/assets/a992aecd-a4a3-4a3d-92fa-28fa31a988ab" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="394" height="128" alt="Screenshot 2025-09-07 090127" src="https://github.com/user-attachments/assets/26789516-53f6-4992-9013-bbf4d49ba1fb" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="419" height="191" alt="Screenshot 2025-09-07 090202" src="https://github.com/user-attachments/assets/59679e8d-2b51-4d68-a3b9-83b3df50c6e4" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="342" height="150" alt="Screenshot 2025-09-07 090227" src="https://github.com/user-attachments/assets/e07183c5-52d9-42a3-a27c-a768a6c314e8" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="412" height="132" alt="Screenshot 2025-09-07 090249" src="https://github.com/user-attachments/assets/ebc7f267-d890-487a-9db2-2f1e5c4f4ee4" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="431" height="129" alt="Screenshot 2025-09-07 090316" src="https://github.com/user-attachments/assets/383c810f-e4c5-410f-8207-01563283cbf7" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="555" height="75" alt="image" src="https://github.com/user-attachments/assets/8400fec2-78de-4f1f-a4f2-2caae3f8ba91" />


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
<img width="555" height="93" alt="image" src="https://github.com/user-attachments/assets/358510aa-8a67-4243-b07c-39fcc17655f2" />


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

<img width="555" height="90" alt="image" src="https://github.com/user-attachments/assets/3d2f92da-afa7-4e09-8c0a-6edf68052948" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="661" height="159" alt="image" src="https://github.com/user-attachments/assets/d0f9b0b1-0564-49e5-83f3-26d3437bd455" />

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

<img width="532" height="83" alt="image" src="https://github.com/user-attachments/assets/de249042-4b7b-473d-bfde-193de91acafe" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="583" height="129" alt="Screenshot 2025-09-07 093818" src="https://github.com/user-attachments/assets/096f67c7-eb81-4143-b90b-8a3e31dc28da" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="410" height="1025" alt="Screenshot 2025-09-07 094426" src="https://github.com/user-attachments/assets/6e605ecb-f1ae-4993-9863-3c2a37b8b737" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1050" height="382" alt="Screenshot 2025-09-07 094446" src="https://github.com/user-attachments/assets/6d58014b-3c20-4415-b0be-4e0985b1a0f0" />

tar -xvf backup.tar
## OUTPUT
<img width="618" height="484" alt="Screenshot 2025-09-07 094503" src="https://github.com/user-attachments/assets/6b75408c-7557-45ec-b5d4-a6f375019dc0" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1245" height="97" alt="Screenshot 2025-09-07 094640" src="https://github.com/user-attachments/assets/685a69c8-8921-4992-8b2f-ae893f1b3b0f" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="825" height="176" alt="Screenshot 2025-09-07 094950" src="https://github.com/user-attachments/assets/2bb55596-25d8-4337-9a44-913a6cff97cc" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="392" height="281" alt="Screenshot 2025-09-07 095100" src="https://github.com/user-attachments/assets/3181319b-7e1f-486f-874f-236190fb56f7" />


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

 <img width="711" height="456" alt="Screenshot 2025-09-07 095724" src="https://github.com/user-attachments/assets/0b2c9fbf-0a24-4c30-b126-b0442f9480f5" />

ls file1
## OUTPUT
<img width="383" height="81" alt="Screenshot 2025-09-07 095738" src="https://github.com/user-attachments/assets/e0d97226-2235-4a40-86fa-0c5daae5b0b8" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="320" height="84" alt="Screenshot 2025-09-07 095757" src="https://github.com/user-attachments/assets/f34e4652-ce96-4493-9030-6df48649c1be" />

abcd
 
echo $?
 ## OUTPUT
<img width="564" height="160" alt="Screenshot 2025-09-07 095820" src="https://github.com/user-attachments/assets/353a95ed-3008-4a24-9a0a-0e17635d49e3" />


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="695" height="217" alt="Screenshot 2025-09-07 100142" src="https://github.com/user-attachments/assets/197f635e-0442-409b-bc1e-042d771f6a57" />


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
<img width="499" height="80" alt="Screenshot 2025-09-07 100615" src="https://github.com/user-attachments/assets/15b788a3-8368-4ee4-a6cc-72253d2fbfc6" />

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

<img width="752" height="159" alt="Screenshot 2025-09-07 103001" src="https://github.com/user-attachments/assets/ee9bb83f-3b44-444e-86ad-81e74799cdfd" />


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
## OUTPUT
<img width="756" height="203" alt="Screenshot 2025-09-07 103249" src="https://github.com/user-attachments/assets/2fd96666-9201-4509-b529-07d56005a5d4" />

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
## OUTPUT
<img width="752" height="159" alt="Screenshot 2025-09-07 103001" src="https://github.com/user-attachments/assets/83a69314-571c-400e-b53c-12f427d65f64" />

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

<img width="729" height="156" alt="Screenshot 2025-09-07 103934" src="https://github.com/user-attachments/assets/5b9debbc-6b1f-488f-a00f-8bc1dabf8a0f" />

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
<img width="756" height="160" alt="Screenshot 2025-09-07 104206" src="https://github.com/user-attachments/assets/73e916f3-ffb6-44af-b443-f51d28357e2a" />

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
## OUTPUT
<img width="888" height="163" alt="Screenshot 2025-09-07 104654" src="https://github.com/user-attachments/assets/6135b5b0-8a2c-4587-a911-f210457359ee" />

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
## OUTPUT
<img width="437" height="364" alt="Screenshot 2025-09-07 120509" src="https://github.com/user-attachments/assets/850694f0-ad0a-4afa-9d11-d5b2453c25a2" />

 
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
 
## OUTPUT
<img width="611" height="230" alt="Screenshot 2025-09-07 120654" src="https://github.com/user-attachments/assets/7727daab-b272-4d0a-a4d5-93f7ccd3a160" />
 
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
 ## OUTPUT
 <img width="639" height="391" alt="Screenshot 2025-09-07 121010" src="https://github.com/user-attachments/assets/9af54e3e-d775-433d-a770-0146051b4fe3" />

 
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
<img width="722" height="106" alt="Screenshot 2025-09-07 121332" src="https://github.com/user-attachments/assets/d427d219-f51e-4bcb-b5b3-047a0ec4aacf" />


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
<img width="382" height="229" alt="Screenshot 2025-09-07 121828" src="https://github.com/user-attachments/assets/a071591a-397a-4947-9687-6bfc03e970ce" />

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
