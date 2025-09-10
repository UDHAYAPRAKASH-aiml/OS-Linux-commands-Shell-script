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

<img width="461" height="159" alt="Screenshot 2025-09-07 143840" src="https://github.com/user-attachments/assets/2af523d9-4ead-4cb8-b4d1-49f3a191aeae" />


cat < file2
## OUTPUT

<img width="409" height="177" alt="Screenshot 2025-09-07 143933" src="https://github.com/user-attachments/assets/c0adc332-790e-4894-8e4b-b0ddd8eadef4" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="454" height="79" alt="Screenshot 2025-09-07 144008" src="https://github.com/user-attachments/assets/3749bfaf-27c9-46a7-a7dd-a4ac1c1dbd92" />

comm file1 file2
 ## OUTPUT
<img width="475" height="234" alt="Screenshot 2025-09-07 144033" src="https://github.com/user-attachments/assets/32dea9c4-87a6-43c9-a363-25307a75605e" />

 
diff file1 file2
## OUTPUT

<img width="422" height="336" alt="Screenshot 2025-09-07 144055" src="https://github.com/user-attachments/assets/d6e866ef-61b5-4331-b6e1-328fabea9ee0" />

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


<img width="350" height="169" alt="Screenshot 2025-09-05 154523" src="https://github.com/user-attachments/assets/32e95baa-7f79-4281-b876-c97e0e0c82b1" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="368" height="129" alt="Screenshot 2025-09-05 154629" src="https://github.com/user-attachments/assets/586d81d7-43d4-4c00-8aa8-9d44174236eb" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="415" height="200" alt="Screenshot 2025-09-05 154635" src="https://github.com/user-attachments/assets/d3b3c15b-9af3-452b-8ccd-9494c094f498" />

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

<img width="350" height="81" alt="Screenshot 2025-09-07 144427" src="https://github.com/user-attachments/assets/79872e8b-6112-47ad-b20e-3dab95fa6dcb" />


grep hello newfile 
## OUTPUT


<img width="367" height="85" alt="Screenshot 2025-09-07 144441" src="https://github.com/user-attachments/assets/776630dd-6654-4db7-b1f6-b5c322b0d75a" />


grep -v hello newfile 
## OUTPUT

<img width="349" height="80" alt="Screenshot 2025-09-07 144518" src="https://github.com/user-attachments/assets/73439e20-e89b-4dd3-9971-b172f5cdbd05" />


cat newfile | grep -i "hello"
## OUTPUT



<img width="425" height="104" alt="Screenshot 2025-09-07 144606" src="https://github.com/user-attachments/assets/947c47a8-95cf-4e1d-b29a-71330100a8ab" />

cat newfile | grep -i -c "hello"
## OUTPUT


<img width="438" height="78" alt="Screenshot 2025-09-07 144629" src="https://github.com/user-attachments/assets/eaa32edc-4e38-46c2-89d7-02ae04208864" />


grep -R ubuntu /etc
## OUTPUT

<img width="1919" height="923" alt="Screenshot 2025-09-05 155243" src="https://github.com/user-attachments/assets/5cece5da-eef3-4d7d-a666-f3d68800fd3a" />


grep -w -n world newfile   
## OUTPUT

<img width="390" height="164" alt="Screenshot 2025-09-05 155350" src="https://github.com/user-attachments/assets/a60299fa-f173-44fc-97a0-c38323b340e5" />

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

<img width="442" height="169" alt="Screenshot 2025-09-05 155558" src="https://github.com/user-attachments/assets/90a46e26-cec3-47d1-993f-a6383e5776a8" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="486" height="169" alt="Screenshot 2025-09-05 155647" src="https://github.com/user-attachments/assets/723fe31b-4708-4189-ba60-263fb28b3beb" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="609" height="173" alt="Screenshot 2025-09-05 155732" src="https://github.com/user-attachments/assets/c5ee3f97-9d8a-49c0-a8cc-54df64c5c3bb" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="373" height="174" alt="Screenshot 2025-09-07 084445" src="https://github.com/user-attachments/assets/be79979f-8da2-4e78-9cc9-fd70eb3cb8d5" />


egrep '(world$)' newfile 
## OUTPUT


<img width="428" height="171" alt="Screenshot 2025-09-07 084520" src="https://github.com/user-attachments/assets/7959bd7b-884a-4cb9-a795-069a3333aaf4" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="463" height="162" alt="Screenshot 2025-09-07 084619" src="https://github.com/user-attachments/assets/3e13e8d1-6aff-41df-8abc-6cf994236d9f" />



egrep '[1-9]' newfile 
## OUTPUT


<img width="393" height="145" alt="Screenshot 2025-09-07 084819" src="https://github.com/user-attachments/assets/1f23ef84-df2e-460f-8aea-98519351198b" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="459" height="149" alt="Screenshot 2025-09-07 084845" src="https://github.com/user-attachments/assets/ac8eaa48-ae40-4bac-ab07-a079743554e6" />


egrep l{2} newfile
## OUTPUT

<img width="358" height="108" alt="Screenshot 2025-09-07 084936" src="https://github.com/user-attachments/assets/18d4068a-1ed1-44a6-a244-cf567967347b" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="356" height="79" alt="Screenshot 2025-09-07 085005" src="https://github.com/user-attachments/assets/244e8400-17fc-465c-b564-ded964dd8312" />


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


<img width="570" height="134" alt="Screenshot 2025-09-07 090426" src="https://github.com/user-attachments/assets/969e4835-a6eb-4f3f-96bb-1260b71626fc" />



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
<img width="444" height="257" alt="Screenshot 2025-09-07 093327" src="https://github.com/user-attachments/assets/695d78b2-a6ad-4dd7-92b9-e55bafcb84c3" />


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

<img width="605" height="241" alt="Screenshot 2025-09-07 093445" src="https://github.com/user-attachments/assets/fbdec300-e676-43a3-b80c-8f49bf1ed0b9" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="537" height="321" alt="Screenshot 2025-09-07 093557" src="https://github.com/user-attachments/assets/fe63b0b4-cb15-468e-957c-09748d2457e6" />

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

<img width="740" height="131" alt="Screenshot 2025-09-07 093739" src="https://github.com/user-attachments/assets/81e9ead5-02b9-4b81-8389-8acd5555580a" />

 
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
<img width="401" height="408" alt="Screenshot 2025-09-07 122053" src="https://github.com/user-attachments/assets/f200b26e-55e4-4a75-a10c-cfd5a5e54f63" />

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
<img width="404" height="229" alt="Screenshot 2025-09-07 122316" src="https://github.com/user-attachments/assets/a3d90d60-96f0-4f10-9553-d9113df3fc30" />

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
 <img width="540" height="211" alt="Screenshot 2025-09-07 122608" src="https://github.com/user-attachments/assets/8ddc8c7b-5fac-4ae2-96a7-d46e459ef998" />

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
<img width="540" height="211" alt="Screenshot 2025-09-07 122608" src="https://github.com/user-attachments/assets/03d190ff-d9ec-4e3a-a42e-21eee321c97c" />


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
<img width="460" height="510" alt="Screenshot 2025-09-07 141043" src="https://github.com/user-attachments/assets/cd18cb2d-3f0e-42cb-b25d-d2c606804bb6" />

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
<img width="341" height="249" alt="Screenshot 2025-09-07 141353" src="https://github.com/user-attachments/assets/232efe1f-dec9-463b-96e9-b8b2e942a0d1" />

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
<img width="349" height="120" alt="Screenshot 2025-09-07 141723" src="https://github.com/user-attachments/assets/99e6957c-b28a-4563-ae45-6fce7f946a9a" />

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
 <img width="389" height="380" alt="Screenshot 2025-09-07 142531" src="https://github.com/user-attachments/assets/4dc491b8-6f39-4e11-9ae6-c0f4d3f56a7f" />

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
<img width="432" height="767" alt="Screenshot 2025-09-07 143249" src="https://github.com/user-attachments/assets/f8558fdc-27d3-4652-b6e8-a8548a43a494" />


# RESULT:
The Commands are executed successfully.
