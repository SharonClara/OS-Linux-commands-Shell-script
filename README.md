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
<img width="415" height="141" alt="image" src="https://github.com/user-attachments/assets/eb86c825-2831-487a-9167-ddb5049ce175" />



cat < file2
## OUTPUT

<img width="412" height="166" alt="image" src="https://github.com/user-attachments/assets/577df5f0-66d5-40ab-9b6d-a42ad1afda97" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="452" height="52" alt="image" src="https://github.com/user-attachments/assets/aa95b633-1f4a-49fb-8e89-0fa50183f96f" />


comm file1 file2
 ## OUTPUT
 <img width="455" height="242" alt="image" src="https://github.com/user-attachments/assets/18490b88-d9cf-4d7b-a3d2-1cd6f5ccaf3a" />


 
diff file1 file2
## OUTPUT
<img width="447" height="186" alt="image" src="https://github.com/user-attachments/assets/9ceea05e-11b8-48ae-b64b-ddec1374aee1" />


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
<img width="456" height="79" alt="image" src="https://github.com/user-attachments/assets/e542377f-926f-43f9-9c5b-71e05cdb9ec2" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="453" height="98" alt="image" src="https://github.com/user-attachments/assets/f16e6794-448d-4f9d-a1ab-77725efe0bea" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="455" height="98" alt="image" src="https://github.com/user-attachments/assets/ae16b36e-44ec-4245-b103-c91c6d63fd2a" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep hello newfile 
## OUTPUT
<img width="458" height="45" alt="image" src="https://github.com/user-attachments/assets/d0f11bb4-5aea-48c1-bdff-3a92f909163b" />




grep -v hello newfile 
## OUTPUT
<img width="458" height="60" alt="image" src="https://github.com/user-attachments/assets/28e24d10-ed13-4c6d-9718-82f7152d7b41" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="458" height="60" alt="image" src="https://github.com/user-attachments/assets/364a7a2b-aa06-4b19-b16d-46aefa3a83a9" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="477" height="65" alt="image" src="https://github.com/user-attachments/assets/995ab343-3853-4299-8b8f-c0ea8e15e3b1" />




grep -R ubuntu /etc
## OUTPUT
<img width="1240" height="375" alt="image" src="https://github.com/user-attachments/assets/234c2f66-5bc6-4ffd-b99a-db074180f032" />




grep -w -n world newfile   
## OUTPUT
<img width="1248" height="85" alt="image" src="https://github.com/user-attachments/assets/b6be83aa-f379-497e-9c16-cb0667a79a53" />



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
<img width="1248" height="85" alt="image" src="https://github.com/user-attachments/assets/f2a672dc-6545-4eba-a359-4aed00853c9a" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1249" height="67" alt="image" src="https://github.com/user-attachments/assets/2e5d4b7c-ca33-49e4-a5e9-38f65268bda0" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1251" height="84" alt="image" src="https://github.com/user-attachments/assets/f378e449-4156-4b48-a980-7853d5ab7dba" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="1245" height="42" alt="image" src="https://github.com/user-attachments/assets/86ad7d3f-3a41-4234-bf50-71639f298dd9" />




egrep '(world$)' newfile 
## OUTPUT
<img width="1247" height="58" alt="image" src="https://github.com/user-attachments/assets/f2806c85-2797-44c0-8f8e-91605141ae6a" />




egrep '(World$)' newfile 
## OUTPUT
<img width="1250" height="37" alt="image" src="https://github.com/user-attachments/assets/20cf2edf-0c58-4f47-aa4e-1113fcb90ef0" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1244" height="74" alt="image" src="https://github.com/user-attachments/assets/e3eddc3b-dd45-4ad8-911f-7ec9276cfc57" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1241" height="43" alt="image" src="https://github.com/user-attachments/assets/fa75c89f-f838-4156-8950-7cb88c42c5b0" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1241" height="60" alt="image" src="https://github.com/user-attachments/assets/7110f032-0af3-4c96-889a-2a22f6870173" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1243" height="40" alt="image" src="https://github.com/user-attachments/assets/7dcc3610-b9bf-4097-abaa-8bca12404e8b" />



egrep l{2} newfile
## OUTPUT
<img width="1246" height="57" alt="image" src="https://github.com/user-attachments/assets/7df29daf-ac3a-45a2-bd96-0a56add297ab" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="1242" height="97" alt="image" src="https://github.com/user-attachments/assets/ee7f6c00-1d87-4af9-bdb1-90174e7e5345" />


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
<img width="1241" height="60" alt="image" src="https://github.com/user-attachments/assets/920a2a10-24ef-47f8-af06-4f66fba63f73" />


sed -n -e '$p' file23
## OUTPUT
<img width="525" height="58" alt="image" src="https://github.com/user-attachments/assets/a41a8ed5-7c9f-4b88-9759-36151590be06" />





sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="555" height="187" alt="image" src="https://github.com/user-attachments/assets/29b67045-4955-4ba6-98f1-387ed5db594c" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="555" height="187" alt="image" src="https://github.com/user-attachments/assets/1a6b1607-377d-4486-a34f-3e905d3e1d2e" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="555" height="187" alt="image" src="https://github.com/user-attachments/assets/dbc86ebc-5897-4b6c-bfc0-2b5c21866f75" />




sed -n -e '1,5p' file23
## OUTPUT

<img width="561" height="134" alt="image" src="https://github.com/user-attachments/assets/a30fe60c-d721-4bcf-81f0-d1231e873cf2" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="556" height="98" alt="image" src="https://github.com/user-attachments/assets/fca643c2-d818-4edd-bc53-35aa31dd8dab" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="553" height="81" alt="image" src="https://github.com/user-attachments/assets/ad0474f7-c8ae-4914-b190-85ba14ad0ab1" />



seq 10 
## OUTPUT
<img width="550" height="222" alt="image" src="https://github.com/user-attachments/assets/becf6e12-01d3-4e70-9a0f-2f9fbbf16257" />




seq 10 | sed -n '4,6p'
## OUTPUT

<img width="553" height="102" alt="image" src="https://github.com/user-attachments/assets/ffb959cb-3cbd-4792-ab77-331814b4e9a6" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="553" height="102" alt="image" src="https://github.com/user-attachments/assets/f4a3c7cc-28ac-41b6-9382-f9a5477b2325" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="552" height="115" alt="image" src="https://github.com/user-attachments/assets/f47e02b8-74bd-4514-8d76-d91039a4e264" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="554" height="100" alt="image" src="https://github.com/user-attachments/assets/218cdce5-14ca-4dc2-8322-f6f33d10b833" />



seq 10 | sed '2,9c hello'
## OUTPUT

<img width="554" height="100" alt="image" src="https://github.com/user-attachments/assets/825601e8-674f-499a-a069-1d8597a78b5d" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="554" height="100" alt="image" src="https://github.com/user-attachments/assets/50880111-6420-4d23-819c-07ac3c0c60d9" />




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="554" height="100" alt="image" src="https://github.com/user-attachments/assets/15c972ab-fb57-4442-97ef-1593562faddb" />



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

<img width="562" height="162" alt="image" src="https://github.com/user-attachments/assets/83bd9df0-7b52-44af-8b1c-d3b2a258ca0d" />


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

<img width="570" height="136" alt="image" src="https://github.com/user-attachments/assets/0eb09984-c6d6-4432-8ef5-60cbc5cdd698" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="563" height="189" alt="image" src="https://github.com/user-attachments/assets/d7b9034a-3693-43bb-86aa-a495bab27996" />


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
## OUTPUT

<img width="421" height="117" alt="image" src="https://github.com/user-attachments/assets/0cfbe652-dd68-484a-bda5-78cc4a528585" />



cat urllist.txt | tr -d ' '
 ## OUTPUT

 <img width="560" height="118" alt="image" src="https://github.com/user-attachments/assets/8c91d0a0-ad89-4334-9c30-9e8559a57c03" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="574" height="116" alt="image" src="https://github.com/user-attachments/assets/5f49ef2a-d6bb-4417-b791-7efdd6e8a024" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="572" height="588" alt="image" src="https://github.com/user-attachments/assets/482c53fe-908f-47b3-815a-04a60aed7136" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="981" height="675" alt="image" src="https://github.com/user-attachments/assets/547a7cad-1498-4927-8187-bec38e994f42" />


tar -xvf backup.tar
## OUTPUT

<img width="981" height="675" alt="image" src="https://github.com/user-attachments/assets/75edfd5e-c410-4050-a281-c68a7c709320" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="980" height="63" alt="image" src="https://github.com/user-attachments/assets/de6a4d90-466b-4000-96c2-53f4dd0c7361" />


gunzip backup.tar.gz
## OUTPUT

<img width="1851" height="135" alt="image" src="https://github.com/user-attachments/assets/b8fb41d3-fe1c-4a98-9374-b60792b0febb" />

 
# Shell Script

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1852" height="189" alt="image" src="https://github.com/user-attachments/assets/7c6c58e5-aaf8-4ec3-80d8-9ded007663c3" />



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

<img width="1853" height="222" alt="image" src="https://github.com/user-attachments/assets/f9025c81-f9b1-48b6-ae5a-d9278e1684b1" />


 
ls file1
## OUTPUT
<img width="1851" height="67" alt="image" src="https://github.com/user-attachments/assets/e3ded558-c63d-4432-8a98-2d4b2387ac58" />


echo $?
## OUTPUT 

<img width="1850" height="66" alt="image" src="https://github.com/user-attachments/assets/b92dbcb1-6371-45b7-95d1-93786c94a888" />

./one
bash: ./one: Permission denied
 
echo $?

abcd
## OUTPUT 

<img width="1856" height="204" alt="image" src="https://github.com/user-attachments/assets/e4de9cfb-b609-4327-a6a4-2546e86ecfc8" />


echo $?
## OUTPUT 


 <img width="1856" height="204" alt="image" src="https://github.com/user-attachments/assets/e4de9cfb-b609-4327-a6a4-2546e86ecfc8" />



 
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

<img width="1852" height="188" alt="image" src="https://github.com/user-attachments/assets/5cef9faa-1820-4bae-a633-7ea5f812a119" />






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

<img width="1848" height="482" alt="image" src="https://github.com/user-attachments/assets/ab5d7f49-15ca-4573-b518-1f5ae141a0eb" />




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

<img width="1851" height="369" alt="image" src="https://github.com/user-attachments/assets/61eba136-4356-48f7-a6a5-f9adc8de824d" />



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

<img width="1845" height="459" alt="image" src="https://github.com/user-attachments/assets/dce45a31-efa0-4df4-ace0-ac33e2388b94" />


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

<img width="1848" height="442" alt="image" src="https://github.com/user-attachments/assets/5cf10068-4929-47ec-b973-f803a4d70811" />


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
<img width="1843" height="244" alt="image" src="https://github.com/user-attachments/assets/e4ca8a4f-ca84-41db-bc1b-819de61ffec7" />


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

<img width="1844" height="298" alt="image" src="https://github.com/user-attachments/assets/0b357036-cd91-4fec-af63-852e5e13d4e6" />



 
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

<img width="1844" height="408" alt="image" src="https://github.com/user-attachments/assets/eb6e7b01-c301-4da9-87ed-177106a8fc4a" />


 
 
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
<img width="1843" height="353" alt="image" src="https://github.com/user-attachments/assets/b85c2d9c-76a2-4c7a-9a64-ebe6d101f812" />


 
 
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

 <img width="1842" height="334" alt="image" src="https://github.com/user-attachments/assets/f46343eb-acb5-41f5-b3a7-72e12d06de65" />


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
## OUTPUT

<img width="1845" height="281" alt="image" src="https://github.com/user-attachments/assets/0eabc417-698b-4749-b61b-c7f89acb2c2c" />


 
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
## OUTPUT

<img width="1843" height="370" alt="image" src="https://github.com/user-attachments/assets/c753b1ba-5f1b-49cc-a2aa-3237293cf64f" />


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

<img width="1844" height="282" alt="image" src="https://github.com/user-attachments/assets/305642e0-9d39-4d86-b574-afff9095069a" />

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

<img width="1844" height="282" alt="image" src="https://github.com/user-attachments/assets/2eaccef3-99b7-4bc0-88a5-78444c71efda" />


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

 <img width="1847" height="478" alt="image" src="https://github.com/user-attachments/assets/0cf91fbf-6dc1-45d7-8bbb-de7ae4289fd8" />


 
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

<img width="1851" height="350" alt="image" src="https://github.com/user-attachments/assets/aea89c48-f54b-4517-884f-2bf10d46ff0f" />


cat forcontinue.sh 
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

<img width="1848" height="386" alt="image" src="https://github.com/user-attachments/assets/435d866b-7cfc-46ca-a6b6-431af2b3136e" />


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

<img width="1853" height="210" alt="image" src="https://github.com/user-attachments/assets/72493ed1-abb8-4402-9da1-808ad1bc5d90" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="1843" height="210" alt="image" src="https://github.com/user-attachments/assets/b38a101f-9fe1-4350-a959-bbc7e87fe903" />




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

<img width="1847" height="459" alt="image" src="https://github.com/user-attachments/assets/16b76517-29b2-4fad-b2a0-e94b8eeb64f5" />


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

<img width="1842" height="300" alt="image" src="https://github.com/user-attachments/assets/b8a4bba4-cb9b-4542-b797-6549512172f2" />

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
<img width="1843" height="691" alt="image" src="https://github.com/user-attachments/assets/23de71f3-f26d-4b73-89f8-8062508f4b60" />


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
<img width="1845" height="618" alt="image" src="https://github.com/user-attachments/assets/1e2e24b4-07aa-4a63-8d9e-48761328dbc7" />



# RESULT:
The Commands are executed successfully.
