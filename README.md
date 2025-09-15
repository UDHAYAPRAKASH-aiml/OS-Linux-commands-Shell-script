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
<img width="564" height="40" alt="image" src="https://github.com/user-attachments/assets/54f6f11c-3baf-4db5-88ae-d2d3d00dc9e0" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="564" height="132" alt="image" src="https://github.com/user-attachments/assets/d159f8f6-9f82-4156-ad6d-f522cbead41e" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="564" height="163" alt="image" src="https://github.com/user-attachments/assets/a0e0af51-fafc-4e65-8963-ada1225c4911" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="564" height="96" alt="image" src="https://github.com/user-attachments/assets/3132d2ef-8ba8-429d-904f-db6bd685af74" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="564" height="57" alt="image" src="https://github.com/user-attachments/assets/f520a971-3c1e-43eb-a58c-e1554dde2564" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="644" height="44" alt="image" src="https://github.com/user-attachments/assets/14a62d8c-3a68-4367-84bd-7e099e08fb06" />


seq 10 
## OUTPUT

<img width="443" height="167" alt="image" src="https://github.com/user-attachments/assets/d0601596-2e5c-4f90-94d5-f525a18d5136" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="598" height="63" alt="image" src="https://github.com/user-attachments/assets/b49e2ea1-771e-4631-8ddf-5886d8ec0666" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="794" height="60" alt="image" src="https://github.com/user-attachments/assets/cf2e37c4-4936-48ae-a6b0-2f74ac15eff2" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="794" height="76" alt="image" src="https://github.com/user-attachments/assets/b93a67b3-966b-4971-8f49-3d066ae55be6" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="794" height="61" alt="image" src="https://github.com/user-attachments/assets/daa207bf-0d47-4a1c-821e-295edda4be1b" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="550" height="56" alt="image" src="https://github.com/user-attachments/assets/07cb015f-b61c-47c2-afeb-d892e51ad58f" />

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
<img width="645" height="63" alt="image" src="https://github.com/user-attachments/assets/d8665dca-6f75-49fe-9111-2bce89a4fea3" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="645" height="453" alt="image" src="https://github.com/user-attachments/assets/f35fbf56-deb5-4076-a890-925f9cccffd2" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="645" height="261" alt="image" src="https://github.com/user-attachments/assets/877535c9-108d-4f9c-baa2-44f252969671" />

tar -xvf backup.tar
## OUTPUT
<img width="559" height="202" alt="image" src="https://github.com/user-attachments/assets/07ee5b1b-108f-4c61-822b-0df87c2097b8" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="659" height="90" alt="image" src="https://github.com/user-attachments/assets/0331343c-9f8a-40d1-ada1-b176d138d034" />



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="631" height="44" alt="image" src="https://github.com/user-attachments/assets/560aa53a-7278-427f-b4e5-f9acdccf8cd7" />


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="565" height="59" alt="image" src="https://github.com/user-attachments/assets/5b071ea1-6844-47d6-bd75-371c8aa83048" />


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

 <img width="591" height="249" alt="image" src="https://github.com/user-attachments/assets/35bb2cf5-1176-4058-9d95-5b5c19232fdd" />

ls file1
## OUTPUT
<img width="474" height="33" alt="image" src="https://github.com/user-attachments/assets/676fc1fa-7883-4666-b365-a1f547bc8511" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="474" height="33" alt="image" src="https://github.com/user-attachments/assets/0f5572ab-3881-44ee-8f74-582802a73d2f" />




 
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
<img width="578" height="83" alt="image" src="https://github.com/user-attachments/assets/2aaf0a6a-bd3e-4739-b740-2722f1c5752b" />


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
<img width="537" height="38" alt="image" src="https://github.com/user-attachments/assets/a1c684bd-7dc2-4c82-b051-8f0526afa88e" />


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

<img width="535" height="39" alt="image" src="https://github.com/user-attachments/assets/098f2c1b-31e0-429b-b135-857d9aa3947e" />



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
<img width="580" height="61" alt="image" src="https://github.com/user-attachments/assets/7d5741be-8c80-47c1-aafc-c4b93875cb41" />

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
<img width="627" height="47" alt="image" src="https://github.com/user-attachments/assets/402f873c-b8b5-4dcb-8060-02a7dd099723" />


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

<img width="627" height="60" alt="image" src="https://github.com/user-attachments/assets/0ec0f229-06ea-49ee-8bf4-81f8cb019c9f" />

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
<img width="627" height="60" alt="image" src="https://github.com/user-attachments/assets/547f455a-ba5f-4b58-8e8c-788842eed7fa" />


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
<img width="657" height="192" alt="image" src="https://github.com/user-attachments/assets/90721f9a-62e6-4df8-a316-c34c82d2cae3" />


 
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
<img width="514" height="89" alt="image" src="https://github.com/user-attachments/assets/604318d5-ed15-42d0-b863-55b958f80dd7" />

 
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
 <img width="514" height="157" alt="image" src="https://github.com/user-attachments/assets/313d323a-6465-44b6-84df-e9a18fc112d1" />

 
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
<img width="540" height="220" alt="image" src="https://github.com/user-attachments/assets/38738868-853a-45da-8312-14827d3cca20" />



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
<img width="540" height="103" alt="image" src="https://github.com/user-attachments/assets/656f9cbd-be76-4254-8887-3021e764effd" />


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
<img width="535" height="231" alt="image" src="https://github.com/user-attachments/assets/d4c643a0-38ba-4639-8727-f6b5c3e485ed" />


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
 <img width="540" height="114" alt="image" src="https://github.com/user-attachments/assets/df3a8b3f-abe2-4d91-be1c-f2825b215846" />


 
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
<img width="535" height="62" alt="image" src="https://github.com/user-attachments/assets/716fd9c8-2710-4044-aedf-1227f4861bc0" />


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
 <img width="491" height="72" alt="image" src="https://github.com/user-attachments/assets/7da658b2-d289-4c67-a3c0-d906086820bd" />


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
<img width="545" height="110" alt="image" src="https://github.com/user-attachments/assets/9e36eda7-e227-4497-9826-f42658f11264" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

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
<img width="503" height="48" alt="image" src="https://github.com/user-attachments/assets/513b9896-702b-4cbb-b6a8-3728bc0c63c8" />



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
<img width="503" height="154" alt="image" src="https://github.com/user-attachments/assets/1e7c411e-e86c-402a-b0b9-138a75b7dbb9" />

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
<img width="503" height="79" alt="image" src="https://github.com/user-attachments/assets/bae13126-bc18-4e02-b5e6-c543187948a5" />


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
<img width="523" height="249" alt="image" src="https://github.com/user-attachments/assets/04848c8d-92a0-406a-9f2b-9352ae763361" />

 
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
<img width="606" height="183" alt="image" src="https://github.com/user-attachments/assets/e6e4d46f-0dbe-4f4b-8c0b-e48ff4e981fe" />




# RESULT:
The Commands are executed successfully.
