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
<img width="571" height="115" alt="image" src="https://github.com/user-attachments/assets/3756c3e8-3f6e-4ede-8c4f-4483283107b6" />



cat < file2
## OUTPUT
<img width="578" height="125" alt="image" src="https://github.com/user-attachments/assets/8fe48623-f660-4715-82d0-7e0151e9a3e7" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="596" height="46" alt="image" src="https://github.com/user-attachments/assets/0155db42-6877-49b3-819e-cc0a7f48df87" />

comm file1 file2
 ## OUTPUT
<img width="622" height="311" alt="image" src="https://github.com/user-attachments/assets/057e774d-a034-4129-831f-bd22f199e7e4" />

 
diff file1 file2
## OUTPUT
<img width="610" height="220" alt="image" src="https://github.com/user-attachments/assets/a7189f0c-4a97-4540-92d7-8be448825249" />


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
<img width="592" height="61" alt="image" src="https://github.com/user-attachments/assets/de7775a8-e57d-413d-975e-0055de7226e1" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="623" height="102" alt="image" src="https://github.com/user-attachments/assets/fad8f256-0282-47bb-95fe-2f7e70101a9f" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="618" height="110" alt="image" src="https://github.com/user-attachments/assets/eb06f2b1-c8e1-40cb-9a62-907a667a3b45" />


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="612" height="70" alt="image" src="https://github.com/user-attachments/assets/a20e65a7-3986-4bb4-b990-d9d74edcff0e" />



grep hello newfile 
## OUTPUT
<img width="613" height="90" alt="image" src="https://github.com/user-attachments/assets/688cf2d4-c60f-4e50-ada5-43819e9e1302" />




grep -v hello newfile 
## OUTPUT
<img width="671" height="62" alt="image" src="https://github.com/user-attachments/assets/31ad0ea8-cb6f-4a66-9a16-ed67c4db6c0d" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="700" height="65" alt="image" src="https://github.com/user-attachments/assets/e27706fb-1fbb-4764-9ff8-50676e6bb876" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="700" height="62" alt="image" src="https://github.com/user-attachments/assets/6000af04-f848-414d-8794-2d7518d7be02" />



grep -R ubuntu /etc
## OUTPUT
<img width="726" height="610" alt="image" src="https://github.com/user-attachments/assets/539a01fd-d655-4a6a-afa1-8f263bed73f4" />



grep -w -n world newfile   
## OUTPUT
<img width="663" height="56" alt="image" src="https://github.com/user-attachments/assets/433dbc66-3f8d-4cf4-add8-f40168999046" />


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

<img width="710" height="65" alt="image" src="https://github.com/user-attachments/assets/569ceb23-54e3-4361-9bda-13c7a2569698" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="697" height="53" alt="image" src="https://github.com/user-attachments/assets/2f446a7b-5c42-4d01-b877-bf6f4e637128" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="727" height="90" alt="image" src="https://github.com/user-attachments/assets/e3a648a4-b32c-4a0d-9875-1ccf3ac77e7d" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="692" height="41" alt="image" src="https://github.com/user-attachments/assets/e88d4113-da03-4f55-9ab6-945b5c353168" />



egrep '(world$)' newfile 
## OUTPUT
<img width="695" height="65" alt="image" src="https://github.com/user-attachments/assets/f7d93ca4-f999-4d18-a6ce-81f56b2e8640" />



egrep '(World$)' newfile 
## OUTPUT
<img width="683" height="47" alt="image" src="https://github.com/user-attachments/assets/49c808cc-cdac-4f0c-8f14-5626ef80f6c6" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="705" height="87" alt="image" src="https://github.com/user-attachments/assets/9de1187c-2f40-4311-a863-85929a9a358e" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="682" height="37" alt="image" src="https://github.com/user-attachments/assets/65ff8e50-a71c-453f-8519-ad336fedb771" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="697" height="50" alt="image" src="https://github.com/user-attachments/assets/34ac8698-ee22-4c24-9d1e-b0caff6280f3" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="707" height="57" alt="image" src="https://github.com/user-attachments/assets/a3b925b1-f03a-42f1-8f4f-9de13dd7b727" />


egrep l{2} newfile
## OUTPUT
<img width="642" height="61" alt="image" src="https://github.com/user-attachments/assets/bb15e266-d6c6-47a8-afb8-cb8f603f40ba" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="672" height="80" alt="image" src="https://github.com/user-attachments/assets/64f50ed0-69e7-4d04-88d8-7555ceda7e01" />


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
<img width="682" height="45" alt="image" src="https://github.com/user-attachments/assets/cc1c94c9-ea4d-4d20-90a4-26367b642ee6" />



sed -n -e '$p' file23
## OUTPUT
<img width="657" height="7" alt="image" src="https://github.com/user-attachments/assets/4e5a99d5-0255-4333-9ae0-f5b0388bc59d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="710" height="200" alt="image" src="https://github.com/user-attachments/assets/1ceaaca8-22fb-4f10-be10-f2a06b947539" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="721" height="198" alt="image" src="https://github.com/user-attachments/assets/d553fa99-eee6-496b-a5c3-58df75b2ea0f" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
=<img width="696" height="222" alt="image" src="https://github.com/user-attachments/assets/f1d2a5f0-e8c1-4908-94f0-8165fd5fc714" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="711" height="137" alt="image" src="https://github.com/user-attachments/assets/13d1b035-25dc-4afb-867c-dc38012175c9" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="700" height="82" alt="image" src="https://github.com/user-attachments/assets/8b59e411-2378-44d6-8cc8-f2863446c413" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="727" height="85" alt="image" src="https://github.com/user-attachments/assets/affa428d-1603-4e29-970a-b7036ccd7c0a" />



seq 10 
## OUTPUT
<img width="596" height="247" alt="image" src="https://github.com/user-attachments/assets/f37c4c1e-c95d-420e-aa9f-8e7773fdef91" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="641" height="92" alt="image" src="https://github.com/user-attachments/assets/47ac1405-ed9e-43c1-8444-8680c6940886" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="695" height="82" alt="image" src="https://github.com/user-attachments/assets/a2b912a3-cd61-4d0f-9483-e7819c845bfa" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="668" height="112" alt="image" src="https://github.com/user-attachments/assets/3e496285-1f3f-449c-8dc9-d1392b6dbdd5" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="666" height="85" alt="image" src="https://github.com/user-attachments/assets/0fee374e-4e79-4beb-9cf0-3fb87b04c37f" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="675" height="93" alt="image" src="https://github.com/user-attachments/assets/fc50b130-aacf-4760-8d93-063e247261b4" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="700" height="90" alt="image" src="https://github.com/user-attachments/assets/5ad75273-f0f7-4578-b6f6-637e2f8cce29" />



sed -n '2,4{s/$/*/;p}' file23
<img width="698" height="80" alt="image" src="https://github.com/user-attachments/assets/95ae0f05-1816-4dcc-b06a-3c6b6ae94543" />


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
<img width="691" height="147" alt="image" src="https://github.com/user-attachments/assets/5d7aec19-9e2b-43b3-9328-a1ee5a2f5ac0" />


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
<img width="691" height="145" alt="image" src="https://github.com/user-attachments/assets/3caca375-6392-40b0-886e-e50e291e7518" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="718" height="215" alt="image" src="https://github.com/user-attachments/assets/064c7935-7d77-4cfe-b492-b5cb81753901" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="672" height="87" alt="image" src="https://github.com/user-attachments/assets/86b435da-615f-445a-966f-b8687a5ccf02" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="723" height="102" alt="image" src="https://github.com/user-attachments/assets/0778599e-93f4-4a29-a4b0-7df426853dac" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="712" height="221" alt="image" src="https://github.com/user-attachments/assets/a5d4df3d-1e6c-4e61-936d-84941c69cfc1" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="692" height="372" alt="image" src="https://github.com/user-attachments/assets/1778c0e6-8f36-4d0f-a27e-47c9487f4cca" />


tar -xvf backup.tar
## OUTPUT
<img width="706" height="215" alt="image" src="https://github.com/user-attachments/assets/9f936af2-d714-463e-91db-ecb55befea94" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="707" height="93" alt="image" src="https://github.com/user-attachments/assets/719a365c-151a-4809-8318-37e96cdd6370" />

gunzip backup.tar.gz
## OUTPUT
<img width="722" height="47" alt="image" src="https://github.com/user-attachments/assets/63c3eea3-16c5-425b-9b59-f4cdb2ce925a" />

 
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
<img width="628" height="126" alt="image" src="https://github.com/user-attachments/assets/928565b2-1945-4d58-9325-0fabbfcec55d" />


cat > scriptest.sh 
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
<img width="645" height="401" alt="image" src="https://github.com/user-attachments/assets/b18cdaf2-7a78-4fd0-9c38-5cc4b9e340fb" />

 
ls file1
## OUTPUT
<img width="570" height="47" alt="image" src="https://github.com/user-attachments/assets/4f18f79c-63df-4b0d-825c-3022019ac68d" />

echo $?
## OUTPUT 
<img width="580" height="37" alt="image" src="https://github.com/user-attachments/assets/bec7e633-7837-492f-aea3-815207bcb102" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="646" height="120" alt="image" src="https://github.com/user-attachments/assets/d6ad1c5a-3e68-4cb2-9cb5-df584866b72a" />

abcd
 
echo $?
 ## OUTPUT
<img width="557" height="115" alt="image" src="https://github.com/user-attachments/assets/5240edf3-01b8-47d0-ba48-84445276918f" />


 
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
<img width="647" height="135" alt="image" src="https://github.com/user-attachments/assets/013cf737-b92b-4d73-8543-b0762b4099d7" />


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
<img width="645" height="192" alt="image" src="https://github.com/user-attachments/assets/1e22c2f4-61af-4385-8147-8ac9e3ca619d" />


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
<img width="597" height="50" alt="image" src="https://github.com/user-attachments/assets/19f6ca4b-df9b-404f-a40e-aa58a40b1fff" />



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
<img width="637" height="115" alt="image" src="https://github.com/user-attachments/assets/98dc8013-7cdc-4751-afc0-f6df8f2847ea" />

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
<img width="661" height="70" alt="image" src="https://github.com/user-attachments/assets/766c66a5-a49c-4f24-a323-6f0dc1823207" />

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
<img width="648" height="126" alt="image" src="https://github.com/user-attachments/assets/3f6516ac-a805-4cdc-a9c0-e2883ec99eba" />

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
 <img width="622" height="167" alt="image" src="https://github.com/user-attachments/assets/b242bfe6-1848-4ebf-8e8d-cce18689dcdc" />

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
 <img width="663" height="192" alt="image" src="https://github.com/user-attachments/assets/db2a1781-9096-4810-b6f5-48bc6675fd40" />

 
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
 
 <img width="657" height="140" alt="image" src="https://github.com/user-attachments/assets/a721f5d3-cf38-451e-b8a5-b253767a152e" />

 
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
 <img width="632" height="302" alt="image" src="https://github.com/user-attachments/assets/b9b5deba-6a02-45b7-adaf-5cfba9d8fc4c" />

 
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
 <img width="657" height="140" alt="image" src="https://github.com/user-attachments/assets/c9e3a701-1c13-4c45-93e9-2e391dee702e" />

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
 <img width="668" height="112" alt="image" src="https://github.com/user-attachments/assets/e7f49309-0140-47a0-9fc5-204257f0a6d6" />

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
<img width="663" height="268" alt="image" src="https://github.com/user-attachments/assets/26e07028-7d72-4802-869b-150fe555867f" />


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
<img width="647" height="103" alt="image" src="https://github.com/user-attachments/assets/a834e7e3-6ed5-4719-905e-5a08bb0e9e6d" />

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
<img width="601" height="247" alt="image" src="https://github.com/user-attachments/assets/2c17451a-e231-4cc1-9fa8-bc7dcb3412b9" />

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
<img width="651" height="477" alt="image" src="https://github.com/user-attachments/assets/bba6b801-b5b9-49ef-9340-27611bf2ca60" />

 
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
<img width="561" height="277" alt="image" src="https://github.com/user-attachments/assets/c9655afe-02a4-4577-80b9-f323de3dedbe" />

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
 cervishnu@TMP215-75-G2:~/myproject/myproject$ #!/bin/bash
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
Iteration number: 1
Iteration number: 2
Iteration number: 4
Iteration number: 5

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
<img width="578" height="152" alt="image" src="https://github.com/user-attachments/assets/cac60755-8222-490b-ba2e-7291a550ae7b" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="541" height="135" alt="image" src="https://github.com/user-attachments/assets/3cfbf8f3-a4f6-4773-957c-9d0516009421" />


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
<img width="595" height="287" alt="image" src="https://github.com/user-attachments/assets/2b3de2c1-14e6-4c21-b0c6-8d082ae622bf" />

 
 ./funcex.sh 1 2
<img width="597" height="45" alt="image" src="https://github.com/user-attachments/assets/7e5b0dc7-9537-4671-873f-2fd4c04bbb9b" />

 
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
 <img width="636" height="261" alt="image" src="https://github.com/user-attachments/assets/393a0005-272b-489e-bf22-94a5d94489aa" />

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
 <img width="587" height="282" alt="image" src="https://github.com/user-attachments/assets/004795f2-f274-4c51-b023-06a0c3c52406" />

 
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
 <img width="626" height="486" alt="image" src="https://github.com/user-attachments/assets/8814c9d7-1dfd-4c3e-8ed4-0c337cc8a014" />

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
<img width="596" height="547" alt="image" src="https://github.com/user-attachments/assets/ca70a107-9b9d-445e-b3d1-ec7526fbbd2c" />


# RESULT:
The Commands are executed successfully.
