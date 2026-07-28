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
<img width="388" height="182" alt="Screenshot 2026-07-28 223353" src="https://github.com/user-attachments/assets/ba276adf-6a11-4cb4-a918-06150249607f" />



cat < file2
## OUTPUT

<img width="333" height="230" alt="Screenshot 2026-07-28 223426" src="https://github.com/user-attachments/assets/fc67c187-1cf4-4a56-9b58-b23975e8a5fc" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="350" height="82" alt="Screenshot 2026-07-28 224411" src="https://github.com/user-attachments/assets/0855de44-4c5d-4ca9-b04c-4954fefa424e" />

comm file1 file2
## OUTPUT
<img width="350" height="212" alt="Screenshot 2026-07-28 224446" src="https://github.com/user-attachments/assets/2083f2b9-5ea7-4546-a58a-67c96b91a434" />


diff file1 file2
## OUTPUT
<img width="322" height="275" alt="Screenshot 2026-07-28 224523" src="https://github.com/user-attachments/assets/89842616-0deb-4759-8b22-b74a4f6bd981" />


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
<img width="340" height="122" alt="Screenshot 2026-07-28 224732" src="https://github.com/user-attachments/assets/d6830bfa-8ea0-4ca8-9f66-09fce0ff15f1" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="305" height="157" alt="Screenshot 2026-07-28 224753" src="https://github.com/user-attachments/assets/f01d5569-113b-45f4-baef-5699fcd1cd39" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="383" height="150" alt="Screenshot 2026-07-28 224806" src="https://github.com/user-attachments/assets/b44e93a4-2c79-4bb5-9a26-7b4d3e4ff990" />


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
<img width="330" height="120" alt="Screenshot 2026-07-28 225352" src="https://github.com/user-attachments/assets/3bde2e91-aba1-4566-ba91-32c8e57b0fc3" />



grep hello newfile 
## OUTPUT
<img width="306" height="72" alt="Screenshot 2026-07-28 225433" src="https://github.com/user-attachments/assets/6c58229d-8310-486e-9aa7-885c6c6e705f" />




grep -v hello newfile 
## OUTPUT
<img width="322" height="70" alt="Screenshot 2026-07-28 225445" src="https://github.com/user-attachments/assets/e8bf3136-f621-478d-9c06-656a77510b22" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="382" height="96" alt="Screenshot 2026-07-28 225541" src="https://github.com/user-attachments/assets/6d215bc7-1a42-4232-83cc-e81202354108" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="412" height="85" alt="Screenshot 2026-07-28 225550" src="https://github.com/user-attachments/assets/f9637c4f-a064-498d-ab51-9bdfc0b38297" />




grep -R ubuntu /etc
## OUTPUT
<img width="648" height="480" alt="Screenshot 2026-07-28 225636" src="https://github.com/user-attachments/assets/07175a64-89d1-452d-8e5e-2b1829f02039" />



grep -w -n world newfile   
## OUTPUT
<img width="347" height="112" alt="Screenshot 2026-07-28 225706" src="https://github.com/user-attachments/assets/0351cc24-5366-469c-a283-7ec1a6717eca" />


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
<img width="377" height="111" alt="Screenshot 2026-07-28 225923" src="https://github.com/user-attachments/assets/f0c4e843-8b4f-45e0-96a2-9184a65ad2d1" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="380" height="110" alt="Screenshot 2026-07-28 230017" src="https://github.com/user-attachments/assets/d1cca4b7-a2b0-4a02-94ce-c266c3e3c9a2" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="417" height="105" alt="Screenshot 2026-07-28 230034" src="https://github.com/user-attachments/assets/7269d306-c78c-4ae4-bf9e-ea87eaac9ed5" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="340" height="77" alt="Screenshot 2026-07-28 230053" src="https://github.com/user-attachments/assets/6dfd735c-f814-4b56-a576-0723d011055d" />



egrep '(world$)' newfile 
## OUTPUT
<img width="347" height="107" alt="Screenshot 2026-07-28 230151" src="https://github.com/user-attachments/assets/8f40ff16-f4d7-4490-aecc-f3188da5ff0c" />



egrep '(World$)' newfile 
## OUTPUT
<img width="357" height="78" alt="Screenshot 2026-07-28 230205" src="https://github.com/user-attachments/assets/93cdf436-5415-430c-b382-aeff1d5c4055" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="388" height="127" alt="Screenshot 2026-07-28 230220" src="https://github.com/user-attachments/assets/abbf3a98-d925-4014-98a7-6504e0649924" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="327" height="77" alt="Screenshot 2026-07-28 230236" src="https://github.com/user-attachments/assets/3c062168-c212-493f-bc8c-e52a0b909d68" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="396" height="77" alt="Screenshot 2026-07-28 230343" src="https://github.com/user-attachments/assets/c2ac7d9c-eec8-40c1-a966-b52322b027c7" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="377" height="87" alt="Screenshot 2026-07-28 230354" src="https://github.com/user-attachments/assets/d7ec1c37-bbb6-49a3-9563-50faf7bc8df4" />


egrep l{2} newfile
## OUTPUT
<img width="311" height="93" alt="Screenshot 2026-07-28 230415" src="https://github.com/user-attachments/assets/5f1a1d72-70b1-46ac-9855-b73ca6d6ea3b" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="320" height="130" alt="Screenshot 2026-07-28 230426" src="https://github.com/user-attachments/assets/51db398b-6b1d-40ad-ba1f-b1b66a2d180a" />


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
<img width="317" height="81" alt="Screenshot 2026-07-28 230546" src="https://github.com/user-attachments/assets/2f54953a-bd1a-4a39-8cbf-a09e304f7de4" />



sed -n -e '$p' file23
## OUTPUT
<img width="301" height="82" alt="Screenshot 2026-07-28 230556" src="https://github.com/user-attachments/assets/d094e243-8700-4064-83cc-351bb1ee0c64" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="363" height="280" alt="Screenshot 2026-07-28 230604" src="https://github.com/user-attachments/assets/8605c8d6-bd09-46b6-affe-e2c176443193" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="360" height="251" alt="Screenshot 2026-07-28 230636" src="https://github.com/user-attachments/assets/451003dd-c35d-4c32-a68d-84dc7a565257" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="406" height="252" alt="Screenshot 2026-07-28 230705" src="https://github.com/user-attachments/assets/6b056509-53c4-4dce-aebe-2d321c4f6c81" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="365" height="185" alt="Screenshot 2026-07-28 230737" src="https://github.com/user-attachments/assets/c1c82d8b-ef7d-45cb-8e9c-26b9f642075e" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="376" height="137" alt="Screenshot 2026-07-28 230747" src="https://github.com/user-attachments/assets/222b96ee-3bdb-4d9e-9a7b-fd1294e780bf" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="413" height="102" alt="Screenshot 2026-07-28 230814" src="https://github.com/user-attachments/assets/c985e4e1-e19d-405f-8cfd-ac89925397d3" />



seq 10 
## OUTPUT
<img width="291" height="312" alt="Screenshot 2026-07-28 230834" src="https://github.com/user-attachments/assets/cd31c2a0-1775-4f03-9e00-32a8ebd5f5c8" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="347" height="127" alt="Screenshot 2026-07-28 230904" src="https://github.com/user-attachments/assets/b27965ab-1a47-4e3e-b81c-00541c81001f" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="342" height="126" alt="Screenshot 2026-07-28 230912" src="https://github.com/user-attachments/assets/0e21ade8-8429-400e-8f3a-3c4292ef27a8" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="346" height="162" alt="Screenshot 2026-07-28 230953" src="https://github.com/user-attachments/assets/eb6dd754-5307-40dc-bef9-5167c826a1f1" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="353" height="132" alt="Screenshot 2026-07-28 231002" src="https://github.com/user-attachments/assets/6a692c77-0d2f-4a1c-8f3c-10e7c4d4cf98" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="353" height="130" alt="Screenshot 2026-07-28 231012" src="https://github.com/user-attachments/assets/90e04002-c8fc-4062-ba86-292e583c16a1" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="418" height="132" alt="Screenshot 2026-07-28 231053" src="https://github.com/user-attachments/assets/db15ae66-822b-47bf-b05a-3f26cce97e89" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="418" height="132" alt="Screenshot 2026-07-28 231053" src="https://github.com/user-attachments/assets/2516ea93-06ff-486a-bde6-8de427a591d1" />


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
<img width="336" height="172" alt="Screenshot 2026-07-28 231312" src="https://github.com/user-attachments/assets/6f1a5109-793a-45f5-a729-0fb7c8b6c6ac" />


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
<img width="332" height="165" alt="Screenshot 2026-07-28 231356" src="https://github.com/user-attachments/assets/49f0a6e6-ad87-409a-8818-128dbfc7aafb" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT
<img width="433" height="262" alt="Screenshot 2026-07-28 231424" src="https://github.com/user-attachments/assets/7f038e72-deb0-414a-9e35-836cf9bb99e7" />

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
<img width="381" height="113" alt="Screenshot 2026-07-28 231536" src="https://github.com/user-attachments/assets/9cc4b229-6c0a-4fd7-8e42-3710aec1459d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="483" height="102" alt="Screenshot 2026-07-28 231607" src="https://github.com/user-attachments/assets/78f8b8e7-0380-484d-a786-8b307658fd1a" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="377" height="302" alt="Screenshot 2026-07-28 231813" src="https://github.com/user-attachments/assets/1db2bf9f-a7b4-4ed8-b0b0-c33f5a8797c8" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="626" height="405" alt="Screenshot 2026-07-28 231854" src="https://github.com/user-attachments/assets/2f5d9f39-01ba-408b-b50c-7c42f36a5c63" />


tar -xvf backup.tar
## OUTPUT
<img width="646" height="412" alt="Screenshot 2026-07-28 231926" src="https://github.com/user-attachments/assets/d302efbd-657b-4788-8246-d43b00c992cc" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="400" height="80" alt="Screenshot 2026-07-28 232801" src="https://github.com/user-attachments/assets/15f4c2b7-a8a2-4a87-bad3-9adaab5ecb9f" />

gunzip backup.tar.gz
## OUTPUT
<img width="648" height="162" alt="Screenshot 2026-07-28 232851" src="https://github.com/user-attachments/assets/7086bc44-6eec-4851-9540-e8c9ecc3d2f1" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="305" height="127" alt="Screenshot 2026-07-28 233000" src="https://github.com/user-attachments/assets/d7f5939e-bb92-41e3-9ddb-125dc3038aea" />


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
<img width="382" height="562" alt="Screenshot 2026-07-28 233112" src="https://github.com/user-attachments/assets/ef17640f-4dad-42dd-86b5-46bdde6cde91" />

 
ls file1
## OUTPUT
<img width="282" height="50" alt="Screenshot 2026-07-28 233155" src="https://github.com/user-attachments/assets/cb106a9f-0683-4aaf-8076-f22b3c0eaba5" />

echo $?
## OUTPUT 
<img width="210" height="77" alt="Screenshot 2026-07-28 233220" src="https://github.com/user-attachments/assets/3d980a55-5147-457f-9f0b-419b9024f511" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="330" height="82" alt="Screenshot 2026-07-28 233328" src="https://github.com/user-attachments/assets/2fd58820-0410-427f-9afc-c30318751783" />
 
abcd
 
echo $?
## OUTPUT
<img width="317" height="77" alt="Screenshot 2026-07-28 233407" src="https://github.com/user-attachments/assets/f2e4f187-5f86-4618-9bf3-ed12011c7da9" />


 
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
<img width="347" height="107" alt="Screenshot 2026-07-28 233459" src="https://github.com/user-attachments/assets/6d5f0c72-65da-4cda-a28e-92c8e8546b73" />


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
<img width="626" height="101" alt="Screenshot 2026-07-28 233529" src="https://github.com/user-attachments/assets/b741d306-83fb-4993-9c83-fbaadc4e0198" />

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

<img width="617" height="171" alt="Screenshot 2026-07-28 234152" src="https://github.com/user-attachments/assets/8b33847c-2e36-400e-9b72-d743931deaaf" />



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

<img width="617" height="171" alt="Screenshot 2026-07-28 234152" src="https://github.com/user-attachments/assets/00989b10-cf72-420b-9359-32dad5aff2f5" />

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

<img width="617" height="171" alt="Screenshot 2026-07-28 234152" src="https://github.com/user-attachments/assets/147cce38-8caa-4e21-a03f-cf4315d6a331" />

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
