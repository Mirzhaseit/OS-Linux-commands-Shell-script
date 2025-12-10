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

<img width="942" height="618" alt="image" src="https://github.com/user-attachments/assets/63fe8f03-0a73-4d1a-a62a-6f17f840682b" />



cat < file2
## OUTPUT

<img width="943" height="624" alt="image" src="https://github.com/user-attachments/assets/3d5c2877-07bc-48e1-a789-f45acd29086b" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="942" height="215" alt="image" src="https://github.com/user-attachments/assets/081fbea3-f428-462a-953b-8e57a57773ef" />




comm file1 file2
 ## OUTPUT
<img width="941" height="434" alt="image" src="https://github.com/user-attachments/assets/54e70136-dca0-414c-900e-ec63b4bdfca4" />


 
diff file1 file2
## OUTPUT

<img width="928" height="409" alt="image" src="https://github.com/user-attachments/assets/9de668eb-eb56-4a5f-a065-9334cc7e71f5" />



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

<img width="794" height="496" alt="image" src="https://github.com/user-attachments/assets/c96488b2-6ac1-4727-b8d1-2f6a249ddcff" />





cut -d "|" -f 1 file22
## OUTPUT

<img width="823" height="346" alt="image" src="https://github.com/user-attachments/assets/2a76766e-6a98-4e11-8338-8d91e8fd81e5" />




cut -d "|" -f 2 file22
## OUTPUT


<img width="790" height="477" alt="image" src="https://github.com/user-attachments/assets/ce565cb7-c590-4f96-b38b-5877efe2b5f2" />




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

<img width="812" height="596" alt="image" src="https://github.com/user-attachments/assets/0ce6c0c7-2e32-4583-b001-3605c3b85f05" />




grep hello newfile 
## OUTPUT

<img width="812" height="596" alt="image" src="https://github.com/user-attachments/assets/5f8557f0-ff8e-482d-bf74-126b51b84912" />





grep -v hello newfile 
## OUTPUT

<img width="822" height="255" alt="image" src="https://github.com/user-attachments/assets/f814f3a5-98d7-4d40-a52f-f82be34b744b" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="816" height="236" alt="image" src="https://github.com/user-attachments/assets/730881a0-c4ba-4756-9e16-527caa3e6748" />





cat newfile | grep -i -c "hello"
## OUTPUT


<img width="800" height="187" alt="image" src="https://github.com/user-attachments/assets/d129ad06-a93c-40fe-aacf-9e7350a26721" />




grep -R ubuntu /etc
## OUTPUT
<img width="819" height="624" alt="image" src="https://github.com/user-attachments/assets/923052df-bea5-4d1d-a5cc-5e09fe425891" />

<img width="815" height="665" alt="image" src="https://github.com/user-attachments/assets/12e63196-4ff3-4444-bbe1-6b95cb947712" />


<img width="802" height="635" alt="image" src="https://github.com/user-attachments/assets/813a5f36-0a41-483b-851a-d0740a24fc0d" />

<img width="897" height="659" alt="image" src="https://github.com/user-attachments/assets/bcbbcacb-b16c-4a99-93cf-a14712e03ead" />






grep -w -n world newfile   
## OUTPUT
<img width="818" height="166" alt="image" src="https://github.com/user-attachments/assets/5845cd9d-2980-45e2-be3e-06250b43be97" />




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

<img width="819" height="210" alt="image" src="https://github.com/user-attachments/assets/465e2254-e870-4748-aff2-a96a287ad45c" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="778" height="164" alt="image" src="https://github.com/user-attachments/assets/e214d6fc-8aaa-4f85-8e42-446705c37aeb" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="861" height="225" alt="image" src="https://github.com/user-attachments/assets/dd9bf6be-ded3-4a58-a9a7-dc8d489b9f8c" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="820" height="144" alt="image" src="https://github.com/user-attachments/assets/b4daed3a-b8ff-4084-af75-e92437e859a8" />




egrep '(world$)' newfile 
## OUTPUT

<img width="829" height="215" alt="image" src="https://github.com/user-attachments/assets/a7bd6ab8-d528-4cdc-b062-89246f1e97c6" />



egrep '(World$)' newfile 
## OUTPUT

<img width="831" height="143" alt="image" src="https://github.com/user-attachments/assets/610744e0-fdb5-4138-8141-48725c76ca79" />




egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="821" height="219" alt="image" src="https://github.com/user-attachments/assets/4bc0a46c-36f9-4229-a13d-99ac3efe11fc" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="813" height="151" alt="image" src="https://github.com/user-attachments/assets/65d30277-0e2f-44ac-8a4f-49e41d9f2c14" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="792" height="340" alt="image" src="https://github.com/user-attachments/assets/1f1804db-7386-4444-b82d-6e30d32639dc" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="792" height="340" alt="image" src="https://github.com/user-attachments/assets/aa1c3a99-238c-4815-9fab-68196d898b61" />




egrep l{2} newfile
## OUTPUT
<img width="792" height="340" alt="image" src="https://github.com/user-attachments/assets/dd453c2f-2fa7-4a51-b282-8c83f00c8d06" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="810" height="187" alt="image" src="https://github.com/user-attachments/assets/6617bc12-3484-4ffd-aa46-73cd0b0dffe6" />



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




sed -n -e '$p' file23
## OUTPUT

<img width="794" height="630" alt="image" src="https://github.com/user-attachments/assets/cdbe7c8e-66a9-4139-84ff-550ce432a167" />





sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="825" height="411" alt="image" src="https://github.com/user-attachments/assets/689e2cee-ccb3-4085-b23f-5d9e241608bc" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="806" height="334" alt="image" src="https://github.com/user-attachments/assets/759ec801-60cd-4616-b550-ea484c9cd241" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="874" height="353" alt="image" src="https://github.com/user-attachments/assets/7fabe5b1-d354-46f0-8248-65c845115c70" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="874" height="241" alt="image" src="https://github.com/user-attachments/assets/eb852c38-adfb-4d96-95ef-1359dc3556e1" />




sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="868" height="187" alt="image" src="https://github.com/user-attachments/assets/a26f5aad-901b-4133-9166-67c693d00a74" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="894" height="180" alt="image" src="https://github.com/user-attachments/assets/8f8e9052-8cf3-41a0-97a0-833c791a70e9" />





seq 10 
## OUTPUT

<img width="825" height="463" alt="image" src="https://github.com/user-attachments/assets/9a845a39-3aa7-4b3a-a722-51531bad697c" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="811" height="609" alt="image" src="https://github.com/user-attachments/assets/fe1663b7-bf20-49a9-a84e-6fd5c832d826" />





seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="811" height="609" alt="image" src="https://github.com/user-attachments/assets/3e4d9290-347a-4e30-b7f1-c46178b75e5d" />




seq 3 | sed '2a hello'
## OUTPUT

<img width="811" height="609" alt="image" src="https://github.com/user-attachments/assets/4b3ab389-040f-4dd8-b54c-ac243379fda9" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="811" height="609" alt="image" src="https://github.com/user-attachments/assets/3f335975-af1b-4400-a8bc-52e59ca40f92" />




seq 10 | sed '2,9c hello'
## OUTPUT
<img width="842" height="183" alt="image" src="https://github.com/user-attachments/assets/091ced4b-1086-4350-933d-28ad6adc2973" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="844" height="180" alt="image" src="https://github.com/user-attachments/assets/c7e2e2d1-6221-4f32-ae17-e29f618cc645" />




sed -n '2,4{s/$/*/;p}' file23


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

<img width="795" height="530" alt="image" src="https://github.com/user-attachments/assets/756de8c0-02fa-445e-9824-10a0f8de6bb8" />



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

<img width="854" height="236" alt="image" src="https://github.com/user-attachments/assets/2c873c45-b164-4a32-9e5a-862203ea7d23" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="846" height="337" alt="image" src="https://github.com/user-attachments/assets/d55af7fc-6167-4bfd-8f2a-beabfaa9fdbe" />



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

<img width="790" height="226" alt="image" src="https://github.com/user-attachments/assets/c3a0910d-685d-4087-8690-37ffc306afbf" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="787" height="247" alt="image" src="https://github.com/user-attachments/assets/d0c82411-2d4e-4329-bb60-34551a629369" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="870" height="430" alt="image" src="https://github.com/user-attachments/assets/ec6c914c-decd-46dd-8ac8-607fe6824a72" />



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="816" height="429" alt="image" src="https://github.com/user-attachments/assets/023586ba-aee0-4155-8cfb-e92b9398ee20" />



tar -xvf backup.tar
## OUTPUT
<img width="826" height="426" alt="image" src="https://github.com/user-attachments/assets/695142d1-b1bc-4436-ab62-168752d22b2c" />



gzip backup.tar

ls .gz
## OUTPUT
<img width="833" height="665" alt="image" src="https://github.com/user-attachments/assets/f7d98950-97f5-4359-bfd0-ea0ae1464f8b" />


 
gunzip backup.tar.gz
## OUTPUT
<img width="833" height="665" alt="image" src="https://github.com/user-attachments/assets/c29eb745-679d-4808-a35f-f8e4bae1df11" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="861" height="226" alt="image" src="https://github.com/user-attachments/assets/9f5e8dbd-644d-4885-a99c-66880f285175" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="799" height="453" alt="image" src="https://github.com/user-attachments/assets/709bc71c-b3fb-4d8c-97b5-90924a9eed9e" />



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
<img width="808" height="511" alt="image" src="https://github.com/user-attachments/assets/ee843174-5849-46f1-a3bf-7b16f316d896" />



 
ls file1
## OUTPUT
<img width="818" height="256" alt="image" src="https://github.com/user-attachments/assets/2cd6c922-e8ca-4441-87eb-44c0e9bd1ddb" />



echo $?
## OUTPUT 
<img width="818" height="256" alt="image" src="https://github.com/user-attachments/assets/4d67c5a5-b3f5-4c0a-9ee7-00bcf2b55970" />



./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
<img width="822" height="146" alt="image" src="https://github.com/user-attachments/assets/028b59e4-37de-4bf3-8033-a339df958afb" />



 
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
![image](https://github.com/user-attachments/assets/3df7ed21-c154-4cd3-89a6-285ead81b28b)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/1045ad7d-9745-4464-82e3-d76012b3e761)


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
![image](https://github.com/user-attachments/assets/4b930435-4abb-40cd-a088-f4cab02bad4c)


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
![image](https://github.com/user-attachments/assets/24322a45-c048-4a66-bd8d-ea749c611486)



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
![image](https://github.com/user-attachments/assets/b24eb56c-c19f-4e02-bc45-11f20f5cbede)


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
![image](https://github.com/user-attachments/assets/b01445b3-9206-4083-af24-4d1cfc2502d4)



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
![image](https://github.com/user-attachments/assets/cd1aa62a-067f-459c-81be-39919a9daa1a)


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
![image](https://github.com/user-attachments/assets/2a35a23e-6e64-4fc6-b959-f377b66acf25)


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
![image](https://github.com/user-attachments/assets/620b3c00-a8a5-4ccd-9989-b1b2fe27f4dd)

 
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
 ![image](https://github.com/user-attachments/assets/eb20e411-016f-4f6f-baef-16787a7d30f7)

 
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
 ![image](https://github.com/user-attachments/assets/ef4144dc-a5c2-46f1-b799-40cb12073d3e)

 
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
 ![image](https://github.com/user-attachments/assets/4e76d522-4f16-454a-954d-f796f775aaa3)

 
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

## OUTPUT
![image](https://github.com/user-attachments/assets/a6b24ec4-7bb2-4bde-a721-c597ef75f674)

 
cat forin3.sh 
```
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
```
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```


$ chmod 777 forinfile.sh

![image](https://github.com/user-attachments/assets/6e44d87a-137a-4d79-9cc2-6e7ef6011eaf)

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
![image](https://github.com/user-attachments/assets/7934026f-f4b3-449f-91ee-247abb2eff01)



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
![image](https://github.com/user-attachments/assets/78654c91-5e21-4518-89c0-b1a3e2696fd5)



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
![image](https://github.com/user-attachments/assets/cc0f4d8d-faf2-4639-9394-481d65f8213f)



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
![image](https://github.com/user-attachments/assets/d08497a9-2281-4004-8b91-2de581c7c0b3)

 
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
![image](https://github.com/user-attachments/assets/dba1e608-c664-454e-bfbe-2eb9e1a01ec4)

 
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
![image](https://github.com/user-attachments/assets/39ac29cf-8e3b-4e71-bc7b-fb80c44561b9)


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

![image](https://github.com/user-attachments/assets/78d106b5-349f-41b9-be1c-7b423b660559)


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

![image](https://github.com/user-attachments/assets/6bbf25ff-deed-4b7a-9b0b-6337b956e486)


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

 ![image](https://github.com/user-attachments/assets/1838e628-eff1-489a-8332-f70bb34bf5fe)


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
 ![image](https://github.com/user-attachments/assets/22c0ccff-9fde-4e3a-a259-da97c8afbd71)

 
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
<img width="821" height="671" alt="image" src="https://github.com/user-attachments/assets/c78a92d1-95bc-4b69-847d-4adfe4158758" />


 
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

<img width="802" height="650" alt="image" src="https://github.com/user-attachments/assets/921a1cb8-c7d4-4bfa-8f58-7da3848a781b" />



# RESULT:
The Commands are executed successfully.
