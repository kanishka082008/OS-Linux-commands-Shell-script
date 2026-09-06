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
<img width="422" height="181" alt="image" src="https://github.com/user-attachments/assets/85c3764f-65ca-43a5-824a-6914300a9b51" />



cat < file2
## OUTPUT
<img width="382" height="197" alt="image" src="https://github.com/user-attachments/assets/5d9e0ce6-8661-42fe-a86a-b98427fa8270" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="426" height="95" alt="image" src="https://github.com/user-attachments/assets/00828879-46e6-4622-b056-ea1a970b2ba1" />

comm file1 file2
 ## OUTPUT
<img width="550" height="292" alt="image" src="https://github.com/user-attachments/assets/ad47e135-1c08-4ba6-8c20-cd0195fa95a6" />

 
diff file1 file2
## OUTPUT
<img width="455" height="317" alt="image" src="https://github.com/user-attachments/assets/19c310b8-8818-4afe-b60f-ce390e0a3665" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
## OUTPUT
<img width="415" height="92" alt="image" src="https://github.com/user-attachments/assets/1bc131dc-7120-46d8-99d6-ef56f0cd0f79" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
## OUTPUT
<img width="437" height="127" alt="image" src="https://github.com/user-attachments/assets/b731a65e-5614-4e09-a001-05b541242a06" />


cut -c1-3 file11
## OUTPUT
<img width="421" height="107" alt="image" src="https://github.com/user-attachments/assets/dee9e8ec-43b6-4744-9ac1-51f263ea34ce" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="425" height="127" alt="image" src="https://github.com/user-attachments/assets/d815891d-1fbf-4d4d-b701-624f7c1364ce" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="366" height="122" alt="image" src="https://github.com/user-attachments/assets/b9048550-afb9-428d-b986-626f20325e9a" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
## OUTPUT
 <img width="437" height="112" alt="image" src="https://github.com/user-attachments/assets/158d920b-6b0c-4485-9b47-72a3c5d97a80" />

grep Hello newfile 
## OUTPUT
<img width="327" height="76" alt="image" src="https://github.com/user-attachments/assets/b5bc6b48-9ef8-4123-9b2f-c2a2bda45df0" />



grep hello newfile 
## OUTPUT
<img width="277" height="137" alt="image" src="https://github.com/user-attachments/assets/51638577-c272-461f-97f8-34dc7476e844" />




grep -v hello newfile 
## OUTPUT
<img width="362" height="77" alt="image" src="https://github.com/user-attachments/assets/63c5b410-455a-4a02-9b02-1c6f4e4bcec6" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="502" height="171" alt="image" src="https://github.com/user-attachments/assets/60636515-374b-4009-8fa2-ad7990264bfd" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="476" height="81" alt="image" src="https://github.com/user-attachments/assets/be97679d-1a7f-473a-8939-093ede1decbf" />




grep -R ubuntu /etc
## OUTPUT
<img width="801" height="557" alt="image" src="https://github.com/user-attachments/assets/ae09ecc8-ebfa-4669-9361-f397f6e0b84f" />



grep -w -n world newfile   
## OUTPUT
<img width="422" height="132" alt="image" src="https://github.com/user-attachments/assets/e27121b6-44a4-471f-be12-42ff8c8d08cb" />


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
## OUTPUT
<img width="502" height="347" alt="image" src="https://github.com/user-attachments/assets/69a62b1e-f677-4a9b-b98a-4115bc444250" />

egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="451" height="131" alt="image" src="https://github.com/user-attachments/assets/3d1dcac4-54e0-4663-aacb-fcbe92c2c439" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="616" height="152" alt="image" src="https://github.com/user-attachments/assets/aeaa6a14-8deb-4095-a395-1ad2528d5455" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="462" height="107" alt="image" src="https://github.com/user-attachments/assets/ce8b77e5-076a-4bdc-bd26-503d1d705449" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="446" height="81" alt="image" src="https://github.com/user-attachments/assets/d4df2506-9ba6-4a7f-9be3-b02114a2c4fe" />



egrep '(world$)' newfile 
## OUTPUT
<img width="452" height="110" alt="image" src="https://github.com/user-attachments/assets/3a4c5b2f-521b-48ee-92f0-1023e643f121" />



egrep '(World$)' newfile 
## OUTPUT
<img width="481" height="80" alt="image" src="https://github.com/user-attachments/assets/97119d37-0589-4811-9205-139fb2a125a2" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="502" height="137" alt="image" src="https://github.com/user-attachments/assets/9c1b0ea0-a206-4a2e-867e-e70da3c41580" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="511" height="82" alt="image" src="https://github.com/user-attachments/assets/3b821cd8-f37c-4f23-84cd-b35cf2e6cbfb" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="502" height="76" alt="image" src="https://github.com/user-attachments/assets/a48bd0b2-40a3-416e-87c4-d1b1b8ca4d2a" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="515" height="82" alt="image" src="https://github.com/user-attachments/assets/76ed0410-e67c-49ea-be99-42f025938e6c" />


egrep l{2} newfile
## OUTPUT
<img width="477" height="106" alt="image" src="https://github.com/user-attachments/assets/1feaaeab-c7bf-4622-ade0-cc97c3b161e4" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="455" height="122" alt="image" src="https://github.com/user-attachments/assets/d461e47f-2f8b-464d-a24c-46846960daf3" />


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
<img width="447" height="86" alt="image" src="https://github.com/user-attachments/assets/0b316301-f984-4433-b938-11d32f29ec9d" />



sed -n -e '$p' file23
## OUTPUT
<img width="505" height="82" alt="image" src="https://github.com/user-attachments/assets/78df2f6d-1ae7-4af9-b13a-9bb193da105d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="535" height="256" alt="image" src="https://github.com/user-attachments/assets/60d0100a-6e60-4d7b-b96f-0c569716ecc5" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="527" height="252" alt="image" src="https://github.com/user-attachments/assets/d0d5aa8a-2d5d-4815-94ef-619f8452bac3" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="602" height="257" alt="image" src="https://github.com/user-attachments/assets/ee87ce34-cf59-4adf-a362-2d01742fed7d" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="476" height="185" alt="image" src="https://github.com/user-attachments/assets/1b4fb9d2-56b2-4822-a00a-98f693e0a41b" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="500" height="132" alt="image" src="https://github.com/user-attachments/assets/d58f0818-927e-41c0-949e-28898ce48930" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="486" height="107" alt="image" src="https://github.com/user-attachments/assets/072f03aa-5e4a-4e65-b3a1-0deab6e68e5b" />



seq 10 
## OUTPUT
<img width="467" height="302" alt="image" src="https://github.com/user-attachments/assets/2c03d7de-631a-4fa2-a526-1a226196cf86" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="422" height="127" alt="image" src="https://github.com/user-attachments/assets/12edc6f2-3fab-4766-aaf6-6aac1a71577b" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="425" height="125" alt="image" src="https://github.com/user-attachments/assets/553fbaee-7bc5-463f-8968-5f6ea69e489e" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="517" height="155" alt="image" src="https://github.com/user-attachments/assets/bccba5b4-df67-4b9d-8c38-cfd686b9d5a4" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="452" height="125" alt="image" src="https://github.com/user-attachments/assets/8eb2e52f-ad62-4c6b-b2d6-953ded484122" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="472" height="127" alt="image" src="https://github.com/user-attachments/assets/beb197c2-f4e0-4a53-bf50-3ad2c68156b7" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="491" height="131" alt="image" src="https://github.com/user-attachments/assets/a3010957-10ce-4383-b28a-d987f97a3a75" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT:
<img width="505" height="136" alt="image" src="https://github.com/user-attachments/assets/dff09f1b-5b37-4d5a-8987-799d9461790b" />


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
<img width="542" height="357" alt="image" src="https://github.com/user-attachments/assets/3edc9f60-074a-47f3-b3f5-7ed82bf6ac41" />


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
<img width="677" height="375" alt="image" src="https://github.com/user-attachments/assets/f93c644b-5c0b-4dfc-a000-632580b51e02" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="532" height="252" alt="image" src="https://github.com/user-attachments/assets/7206006a-160a-4cb1-8961-904ba78ae67e" />

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
## OUTPUT:
<img width="477" height="256" alt="image" src="https://github.com/user-attachments/assets/d1dea4a9-717b-4f2a-aac7-4ec89b04da11" />

cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="491" height="130" alt="image" src="https://github.com/user-attachments/assets/ff8a3926-ef09-4d71-a05c-a0acf390ac35" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="552" height="132" alt="image" src="https://github.com/user-attachments/assets/46099f13-9ea6-4a67-8645-9886d810b975" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="670" height="702" alt="image" src="https://github.com/user-attachments/assets/b8f70164-1807-4daa-b98b-cea5750cd332" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="807" height="702" alt="Screenshot 2026-07-27 215037" src="https://github.com/user-attachments/assets/0279c30b-364f-478a-9010-2f4c1578a1ed" />


tar -xvf backup.tar
## OUTPUT
<img width="738" height="693" alt="Screenshot 2026-07-27 215111" src="https://github.com/user-attachments/assets/947ebe0a-8cdd-43f9-ad12-8cfc7112be7b" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="547" height="122" alt="Screenshot 2026-07-27 215222" src="https://github.com/user-attachments/assets/c791fdba-9e03-44ae-8c63-ed75e578be56" />
 

gunzip backup.tar.gz
## OUTPUT
<img width="436" height="92" alt="Screenshot 2026-07-27 215243" src="https://github.com/user-attachments/assets/b496290a-72f9-4cda-a2c8-9a00e22fb8d0" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="516" height="227" alt="image" src="https://github.com/user-attachments/assets/51fba364-2a53-407b-9401-f65b0ca45980" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="452" height="272" alt="image" src="https://github.com/user-attachments/assets/d47add4b-8c00-4b09-b970-5ab9799a53df" />


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
<img width="707" height="347" alt="image" src="https://github.com/user-attachments/assets/4f052c9c-c23a-4dc6-b9a7-e8862abd075f" />


 
ls file1
## OUTPUT
<img width="293" height="74" alt="image" src="https://github.com/user-attachments/assets/bf21dd0c-5c06-422a-8398-35b774381c51" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
<img width="377" height="75" alt="image" src="https://github.com/user-attachments/assets/38390637-dff0-48d0-80c0-0facf4827b10" />

 
echo $?
## OUTPUT 
<img width="367" height="80" alt="image" src="https://github.com/user-attachments/assets/cfe4d8eb-5aad-4f0c-94f8-dc59d6378cd9" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="367" height="80" alt="image" src="https://github.com/user-attachments/assets/ff9cb5e4-90b9-4465-ba3c-5b91ded86c0e" />


 
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
## OUTPUT
<img width="827" height="281" alt="image" src="https://github.com/user-attachments/assets/b95d35a9-0c40-4073-8c49-5a2da36cb6f7" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="677" height="156" alt="image" src="https://github.com/user-attachments/assets/703409e0-0a4b-475a-8de6-10ee97365d44" />


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
<img width="750" height="237" alt="image" src="https://github.com/user-attachments/assets/b2021d18-d456-4669-b7db-5384fe4a3156" />

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
<img width="657" height="475" alt="image" src="https://github.com/user-attachments/assets/2e0b56e0-c8c7-406d-b79f-46d9519f8356" />



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
<img width="613" height="166" alt="image" src="https://github.com/user-attachments/assets/f3433adc-ed5f-43f3-8012-e7674971cd6c" />

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
<img width="791" height="200" alt="image" src="https://github.com/user-attachments/assets/86fc2cd3-99a6-452e-b54f-e30562ed27fc" />

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
<img width="782" height="167" alt="image" src="https://github.com/user-attachments/assets/ea2d12b1-7b6f-443a-969c-b2d48df7c236" />


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
<img width="890" height="177" alt="image" src="https://github.com/user-attachments/assets/817aabcb-4be9-4746-80a4-f266fae602de" />

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
## OUTPUT:
<img width="587" height="137" alt="image" src="https://github.com/user-attachments/assets/9dede2a9-ddb1-42ea-b083-3134229e66a0" />


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
 ## OUTPUT:
 <img width="366" height="339" alt="image" src="https://github.com/user-attachments/assets/70df3b4e-eec5-4e7d-bffc-ac8f141a91d3" />

 
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
## OUTPUT:
<img width="671" height="237" alt="image" src="https://github.com/user-attachments/assets/6a3147dd-ab0e-4ec1-b5d5-25c6088ed331" />

 
 
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
 ## OUTPUT:
 <img width="682" height="311" alt="image" src="https://github.com/user-attachments/assets/167b7f63-df96-441f-badc-225d14fae7c9" />
 

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

 ## OUTPUT:
<img width="737" height="221" alt="image" src="https://github.com/user-attachments/assets/441af616-b478-4354-8b05-3972e40fb8db" />

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

## OUTPUT:
<img width="842" height="307" alt="image" src="https://github.com/user-attachments/assets/47114637-9a0b-482a-a1b6-ee3a1831b2f1" />

 
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

<img width="551" height="257" alt="image" src="https://github.com/user-attachments/assets/ecf0e380-c59a-476b-886e-bd519963ff06" />

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
```
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```

## OUTPUT
<img width="517" height="257" alt="image" src="https://github.com/user-attachments/assets/6f9acb7b-bc53-4491-9a36-18dd8d5d7888" />


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
<img width="600" height="230" alt="image" src="https://github.com/user-attachments/assets/73393767-0cfb-4fda-b8e8-8398177f77af" />

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
<img width="441" height="230" alt="image" src="https://github.com/user-attachments/assets/29b3601e-f19e-4ad0-a24a-26ec33a785de" />

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
<img width="517" height="402" alt="image" src="https://github.com/user-attachments/assets/1d6440da-c151-415d-9017-6bdc4117a650" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

 ## OUTPUT
 <img width="720" height="155" alt="image" src="https://github.com/user-attachments/assets/ff5a968f-14f5-4d2d-ba6e-5baba0f6a128" />

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
 <img width="532" height="197" alt="image" src="https://github.com/user-attachments/assets/b41ea305-b848-4922-adeb-04f6c4a0c832" />

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
<img width="600" height="155" alt="image" src="https://github.com/user-attachments/assets/a6b26d7c-9aaa-4b08-ba18-1da0cdd83829" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
<img width="407" height="127" alt="image" src="https://github.com/user-attachments/assets/859208e1-e2f5-4b7a-bd20-353060b2fecd" />




 
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
 ./funcex.sh 
 
 ./funcex.sh 1 2

## OUTPUT
<img width="502" height="210" alt="image" src="https://github.com/user-attachments/assets/ead5ecf8-e5fa-4e5b-91d3-cbddc7b0068f" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="309" height="127" alt="image" src="https://github.com/user-attachments/assets/4dee4714-aa72-4d2f-98d0-7cc91205629c" />


 
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
$ ./argshift.sh 1 2 3
## OUTPUT
 <img width="486" height="172" alt="image" src="https://github.com/user-attachments/assets/dcc57f64-f595-4024-8914-0ea759dcde9e" />


 
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
 
 ## OUTPUT:
 <img width="665" height="462" alt="image" src="https://github.com/user-attachments/assets/09ff7b62-33f8-49de-a73a-81aa5d134467" />

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
<img width="472" height="381" alt="image" src="https://github.com/user-attachments/assets/41aee01c-ddae-4604-8dc6-ea7e392d3c16" />
 
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
<img width="590" height="185" alt="image" src="https://github.com/user-attachments/assets/ac9c13f5-8ad4-4f9d-9e84-ff7c2a6288a3" />


# RESULT:
The Commands are executed successfully.
