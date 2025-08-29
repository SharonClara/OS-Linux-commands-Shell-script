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

<img width="473" height="160" alt="437457231-3bdfa2ff-aae9-48e4-9676-c896f9584986" src="https://github.com/user-attachments/assets/523c1181-5523-43bb-9253-45f1af41be6e" />


cat < file2
## OUTPUT

<img width="473" height="179" alt="437457394-af393f30-562b-459a-a506-b6636ae8ef73" src="https://github.com/user-attachments/assets/883d895f-8bf4-4233-8796-54a04de1979a" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="497" height="72" alt="437457530-2280dbd2-062f-46c0-9713-0e8256cd5389" src="https://github.com/user-attachments/assets/9af080b7-282e-4b4a-9057-4cb6af765128" />

comm file1 file2
 ## OUTPUT
<img width="539" height="277" alt="437457649-915fc648-306f-45ba-9d3c-4d8bf7bc5860" src="https://github.com/user-attachments/assets/82e0e224-6db9-43eb-b36c-3bd7fd59af1b" />

 
diff file1 file2
## OUTPUT

<img width="539" height="246" alt="437457756-2c162c44-2331-4484-be17-24ee7de3eaa6" src="https://github.com/user-attachments/assets/bcc5851f-cbaa-4b20-8053-4d7146610963" />

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

<img width="556" height="74" alt="437458281-dd66df9e-c855-4d54-8ef5-b6c8eaabac1d" src="https://github.com/user-attachments/assets/1d9e925f-8e72-4fe8-aac6-bcf1c824419b" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="551" height="119" alt="437458371-cc0a34a8-3206-4976-87c3-dd516d2f6be2" src="https://github.com/user-attachments/assets/6094c47a-af91-46fd-be88-d901902f986e" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="551" height="119" alt="437458492-07a9fea5-2f6b-403c-85e6-3afcad424bd5" src="https://github.com/user-attachments/assets/9a09eae6-4949-437c-936a-444b0d68e547" />

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

<img width="557" height="65" alt="437458616-72b4cae9-4716-4171-877d-d1c479902c29" src="https://github.com/user-attachments/assets/d4864f43-e79e-4608-9a04-159d168a412f" />



grep -v hello newfile 
## OUTPUT

<img width="557" height="65" alt="437458725-8563b624-f3ff-4b03-b1ef-3408646dff32" src="https://github.com/user-attachments/assets/35a54694-965b-4fa9-8f33-165e4f29cbca" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="698" height="88" alt="437458868-52d8b101-4ee2-4256-be9d-fff9f97938bd" src="https://github.com/user-attachments/assets/14853f99-33ef-4bc4-8a4e-dbaf8a171114" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="685" height="66" alt="437458953-b99caa4d-54da-47f4-872a-5532ed9bcc0c" src="https://github.com/user-attachments/assets/8a46bb8e-ac0b-42e8-87cd-2f8b807dda9a" />



grep -R ubuntu /etc
## OUTPUT
<img width="698" height="243" alt="437459041-32462e29-2612-4e62-8a04-c5380e9eaf46" src="https://github.com/user-attachments/assets/49656c77-2184-4a37-a029-613d97816869" />



grep -w -n world newfile   
## OUTPUT
<img width="717" height="83" alt="437459116-e4b93b2b-0ef1-41e4-992a-f763a46d9880" src="https://github.com/user-attachments/assets/7439b7f7-609a-4f0f-8eb0-b83ee48d17f0" />


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
<img width="710" height="79" alt="437464958-e1f86f83-2319-478d-80db-700241f0f4af" src="https://github.com/user-attachments/assets/8295c9e8-f538-4739-b3cc-d8a8c59ef946" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="704" height="68" alt="437465055-dfe22c7d-e206-42d8-b728-b05982e6d64a" src="https://github.com/user-attachments/assets/5d6533c6-8ed7-477f-affe-f73e477c2180" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="710" height="79" alt="437465229-821299ba-abbf-40aa-a103-29e7889efced" src="https://github.com/user-attachments/assets/16d5cbed-d5aa-4680-9513-5e099298249f" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="710" height="61" alt="437465316-05a31db5-dcc1-43d1-95a7-4c91d105035c" src="https://github.com/user-attachments/assets/cf4449a9-753a-4b53-9c95-79d5941bfa2a" />



egrep '(world$)' newfile 
## OUTPUT
<img width="709" height="77" alt="437465425-4350bbdb-c483-4a9e-a078-7cc66765cbb5" src="https://github.com/user-attachments/assets/a16ecb35-335a-4780-9c60-68fcab6082fe" />



egrep '(World$)' newfile 
## OUTPUT
<img width="695" height="64" alt="437465518-e55c7058-7ea3-4166-98ae-8bdd952f2e77" src="https://github.com/user-attachments/assets/f3aabfaf-91c6-4d50-8872-afdb90be5819" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="701" height="104" alt="437465629-c2c00bf5-fc69-46c3-a928-b0014ec3b22b" src="https://github.com/user-attachments/assets/b2db3466-d7b8-4c24-a1b4-2501b4218022" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="697" height="60" alt="437465729-b8b09f7d-2e5f-46e0-9a4b-062967ae9990" src="https://github.com/user-attachments/assets/3f9c740e-54f8-46ed-8820-5b66e9defa57" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="697" height="60" alt="437465831-6e2e6a13-356a-48bb-a901-7e09ef4e56c4" src="https://github.com/user-attachments/assets/944e76f2-8047-4e50-8093-7b782baa3779" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="697" height="60" alt="437465914-87f77de4-ed53-442b-943f-1ef209486db0" src="https://github.com/user-attachments/assets/68712028-6554-40a0-a102-56bad6af387e" />


egrep l{2} newfile
## OUTPUT
<img width="706" height="82" alt="437466037-a37ebe8d-9872-4032-9b76-f6c76473a271" src="https://github.com/user-attachments/assets/27c25d96-ebc0-4bc0-8331-ae1718dcaff5" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="704" height="98" alt="437466106-54852ad3-824b-49d2-8c1f-dd8637fbeb43" src="https://github.com/user-attachments/assets/530613c2-c29c-42ec-8eef-7d37f4d740bf" />

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

<img width="889" height="44" alt="437489295-0b75c716-5f17-43d3-b333-58e50142df07" src="https://github.com/user-attachments/assets/63515cfd-91c7-4cd7-b4ed-1364c0f6ac1b" />

sed -n -e '$p' file23
## OUTPUT
<img width="889" height="44" alt="437490345-a2cd0d2e-7e0d-4225-89de-3502241ed234" src="https://github.com/user-attachments/assets/f8033699-252e-4f00-9816-754c7fbbc6a6" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="940" height="169" alt="437490445-827055f7-d83e-4d35-a153-23badeda6fd6" src="https://github.com/user-attachments/assets/7cafd3bb-0175-46eb-afde-964c4b37482d" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="950" height="169" alt="437490521-98185b26-0a93-43cd-80d0-02adb4acfd86" src="https://github.com/user-attachments/assets/cb51f4a2-3438-40aa-8bca-5954735a5118" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="950" height="169" alt="437490641-3fc7721e-7fed-498d-be9d-3c2bab773221" src="https://github.com/user-attachments/assets/28056cc3-63e0-4166-bdfd-62352ecbc195" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="952" height="117" alt="437490763-e2d186c7-bc87-4d4f-96ca-fd74dee0ea46" src="https://github.com/user-attachments/assets/74f04a5e-95a3-4479-819c-575ebc1497ba" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="951" height="78" alt="437490904-71be1184-ed6b-4964-8c33-28424752b3b9" src="https://github.com/user-attachments/assets/5cb62644-a355-4a05-8988-5c460f194b3a" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="969" height="62" alt="437490987-ce9ca8bf-3f6c-43eb-8185-68e0a1dff120" src="https://github.com/user-attachments/assets/12219fd3-f160-4517-93ba-c80d1ce73931" />



seq 10 
## OUTPUT

<img width="754" height="198" alt="437491760-cc96b5a5-02f6-44e3-bdd1-710072bffd62" src="https://github.com/user-attachments/assets/a395e0da-e116-46f4-b2e9-c5f000aa8279" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="888" height="79" alt="437491904-5851ad1f-c402-421d-826b-a6ff7c51ff7e" src="https://github.com/user-attachments/assets/242ef53f-cd6e-4d13-9d1d-0ea06f399f70" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="892" height="76" alt="437491996-eb0b1e60-a6f0-4bfe-98fe-cb9d618730b6" src="https://github.com/user-attachments/assets/86b3680c-640d-4180-b1ec-0b5599e5dd26" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="891" height="94" alt="437492115-2379f38b-4feb-45e1-b512-9bb32771e599" src="https://github.com/user-attachments/assets/7079a8f8-06c0-4e87-bd52-f4ca50fb208b" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="890" height="82" alt="437492246-833c6a31-2e44-4e27-bb04-947d398b02ca" src="https://github.com/user-attachments/assets/1299d20e-ad86-457f-8c23-52a8d6ca95e9" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="910" height="80" alt="437492341-651c305a-2930-49da-9d6e-b34b7182bd1f" src="https://github.com/user-attachments/assets/41b5155e-aff0-493f-a600-0b91e76a34af" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="954" height="76" alt="437492457-62cdb5a6-2934-4a98-bf05-bad0ad55408a" src="https://github.com/user-attachments/assets/0e006a40-d3f2-4878-922d-6c2cdef003d8" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="954" height="76" alt="437492595-f1321769-245a-4d40-9ee3-3da7ae6e4ef3" src="https://github.com/user-attachments/assets/e712a68c-b941-4e67-a431-96215d7fb61d" />


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
<img width="796" height="112" alt="437493498-261e7f30-415e-4d2d-a05b-a0ba608160b0" src="https://github.com/user-attachments/assets/797fc51a-6ab6-405a-8127-934cca30e05f" />


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
<img width="796" height="112" alt="437493594-7b6917bf-3b1f-4cb0-9010-34cfdaf13e7c" src="https://github.com/user-attachments/assets/b1b76381-05f2-43df-893e-050581684241" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1006" height="169" alt="437493721-ae489164-3769-482c-9b72-4c7e4443bee9" src="https://github.com/user-attachments/assets/7de4b04a-ea3e-49ad-af11-75584e25f79d" />

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
<img width="858" height="74" alt="437493836-b44e0bca-e78e-4175-aeae-6bc10af122ee" src="https://github.com/user-attachments/assets/a8f74687-66e8-48ca-b541-4b2c4d238c7b" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1055" height="76" alt="437494240-4c7ba8e0-d84b-4ad5-828a-48d4614476e4" src="https://github.com/user-attachments/assets/47a433fe-84ed-489e-b017-90e5de3e3f73" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="892" height="363" alt="437494849-8efda15e-5ced-4ce2-a992-3cddeef81b80" src="https://github.com/user-attachments/assets/dda56b33-37d4-4c9b-a1b8-74ae81b0a594" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="967" height="1001" alt="437494971-bdddfcc7-78b1-4d8b-926d-85872cfeca44" src="https://github.com/user-attachments/assets/797ebbe0-c3a2-4608-a662-2fc1b409629c" />


tar -xvf backup.tar
## OUTPUT
<img width="967" height="1001" alt="437495348-6244eb8d-980e-4ee6-b872-e0e1c19c288f" src="https://github.com/user-attachments/assets/e76e2b87-9919-47c6-9a4c-e111a5c42612" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="861" height="44" alt="437495495-d2d3bc71-0aca-4c7b-9eaf-7ac52395bd64" src="https://github.com/user-attachments/assets/b3622def-af35-4fe1-95ea-eb890084f7b5" />

gunzip backup.tar.gz
## OUTPUT
<img width="1662" height="279" alt="437495623-0ee0e9e5-1613-43f2-8e5c-7062c7631a08" src="https://github.com/user-attachments/assets/3ed11304-920e-4e6f-8dfd-8e2a1db00cff" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1110" height="134" alt="437512669-d43e1c06-4292-4f0d-91d0-79389355bfe8" src="https://github.com/user-attachments/assets/ab99915a-943f-49fe-8621-959cfef717b2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="942" height="161" alt="437513073-880f5adc-41d9-4385-bdb0-85eec925813b" src="https://github.com/user-attachments/assets/7b11ea65-fb6b-4ccc-aa32-ea20298dbba6" />


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
<img width="901" height="507" alt="437513340-02e98cb0-0823-4a6d-9841-1a7213aef79b" src="https://github.com/user-attachments/assets/95b4a3b4-63f1-4aab-926d-31de2fe26f11" />

 
ls file1
## OUTPUT
<img width="773" height="35" alt="437513490-2e852b13-1588-45e0-a9b1-ec8e48fab55c" src="https://github.com/user-attachments/assets/eebd4e3f-60ec-4bbe-8224-b8c7030caec0" />

echo $?
## OUTPUT 

 <img width="773" height="45" alt="437513639-2d221705-b0a6-4cff-9c7a-63d35e181b21" src="https://github.com/user-attachments/assets/29722620-fb7d-45c1-aba2-2c224bbe64ce" />
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="769" height="185" alt="437513753-920d7501-867e-4eaf-bf9d-a01369f9f077" src="https://github.com/user-attachments/assets/f02abd9d-33df-4992-bcc7-527f2bc216e2" />


abcd
 
echo $?
 ## OUTPUT
<img width="769" height="185" alt="437513908-6e3ff907-6662-465b-b873-3caf3a85d86c" src="https://github.com/user-attachments/assets/d61b9f2b-fd9a-4f69-a7fe-631d15541b69" />


 
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
<img width="840" height="186" alt="437514068-68445397-8903-455a-8944-05a9c743bb77" src="https://github.com/user-attachments/assets/e04ab174-55de-4a68-b34a-81c012de7bce" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="804" height="45" alt="437514174-8b0a1ae7-8ee9-4d8c-a6da-e0b19d34effc" src="https://github.com/user-attachments/assets/e9baf9a0-2928-4a04-9b67-ad9c3ed4cfcf" />

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
<img width="824" height="47" alt="437514310-a6269750-5552-40c1-a460-c0102d92478b" src="https://github.com/user-attachments/assets/f56d029e-00f9-4755-b8ce-8ee9d648fd2f" />

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
<img width="820" height="82" alt="437514439-7bc5d0e0-8ef8-47b6-9be5-1cb0cb322bf9" src="https://github.com/user-attachments/assets/a7da1d9e-9b74-4a2c-b36a-1eb7fff622cb" />



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
<img width="792" height="62" alt="437514567-bd3fa98c-918f-4fe9-87e8-83aa78955a55" src="https://github.com/user-attachments/assets/ac091df5-c2f3-4ffe-9d29-ce69f2a49d63" />


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
<img width="820" height="82" alt="437514704-0b1ec023-85da-4ffb-bd59-bb43312cfe95" src="https://github.com/user-attachments/assets/4eb32560-08bd-46b8-847a-558f3c3a2c6c" />

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

<img width="823" height="44" alt="437514825-e13003ae-4cf7-4e8a-a9c8-23f36be3cd84" src="https://github.com/user-attachments/assets/3cc8238b-06a3-4684-a71f-c487133e41e4" />

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
<img width="823" height="44" alt="437515548-ba3cd1c8-2e21-42aa-ad1f-7e201567440e" src="https://github.com/user-attachments/assets/63322cb2-865d-4cd5-8ec9-b2f98d3ff9ca" />

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
<img width="823" height="44" alt="437515735-611dd7e7-6094-4ed4-bbc2-dc699bfbec7e" src="https://github.com/user-attachments/assets/2108c85f-3a8f-4ef8-8e83-30f9a6a4a95b" />

 
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
<img width="829" height="203" alt="437516171-766969d6-cdba-4352-b458-bc18ddd0f0d4" src="https://github.com/user-attachments/assets/3f3d7a45-ec1a-4fab-a51b-eb07cf7f8650" />

 
 
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
 <img width="829" height="100" alt="437516323-82ca8200-02c3-4f86-b3af-56fb87280f7c" src="https://github.com/user-attachments/assets/81e1b3e6-5313-4bea-aaf3-17ac7a2f3ba8" />

 
 
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
 
 <img width="789" height="128" alt="437516437-09a67174-2cc7-46ba-bc9e-2045100834c6" src="https://github.com/user-attachments/assets/1297e184-fb73-44c2-bf9d-4ea3475ae323" />

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
<img width="784" height="80" alt="437516569-63454b29-1600-4e43-864f-c532f36c497a" src="https://github.com/user-attachments/assets/4eca85e2-5c20-4cd0-9045-37599e67b651" />

 
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
 <img width="787" height="152" alt="437516740-a73c67cd-2597-46f9-abef-d0b4ae0703bf" src="https://github.com/user-attachments/assets/eba19ad1-4c05-4e94-a158-abf416aadb8f" />

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

<img width="816" height="113" alt="437516934-b80b5ac5-8376-4764-8099-a472f57eccc0" src="https://github.com/user-attachments/assets/34763dfb-c812-4cb2-8bfc-cec3d1415e08" />
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
<img width="823" height="115" alt="437517080-dc4bb67d-df6c-4df8-99f1-6adb34909db2" src="https://github.com/user-attachments/assets/63da27be-630a-44d8-8c28-ba06f92f84cd" />

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
<img width="833" height="236" alt="437517946-22bb8726-77f3-4928-902a-53312da037e3" src="https://github.com/user-attachments/assets/5f9fb35d-f46e-4766-8aa1-07d5285e7719" />

 
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
 <img width="825" height="79" alt="437518303-57b3ca85-f61c-4600-9db7-4488bcabb26e" src="https://github.com/user-attachments/assets/d37b1836-3f60-4977-ad62-bbf06557fbb9" />

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
 <img width="837" height="113" alt="437518629-54fc3698-e66d-4238-9dd7-4eea6acd66b3" src="https://github.com/user-attachments/assets/5cd3e4e9-7a16-4d95-ac68-7d7d2d449378" />

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
<img width="799" height="57" alt="437518886-d518a631-c2f0-4a8c-99aa-99bb59b92783" src="https://github.com/user-attachments/assets/a3d4018b-1982-4a0b-9d5e-c55874e547e4" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="808" height="57" alt="437519922-739e8f84-e5ce-4d44-9376-d9fdb6620001" src="https://github.com/user-attachments/assets/d0bc5b7c-893d-42c3-b67c-3420ea447374" />



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
<img width="807" height="37" alt="437520149-7a77ec0f-e0c6-4f97-95f3-1bc04bc59320" src="https://github.com/user-attachments/assets/c46b88ad-d2fd-4bec-a45f-df5fa172c70d" />

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

 <img width="869" height="72" alt="437521449-49d19cc0-df8d-4b55-9b44-8850ea589337" src="https://github.com/user-attachments/assets/7d2c1963-df95-4b25-bd94-9a433f1f5fd0" />
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
 <img width="895" height="255" alt="437521835-41c21647-4337-4f8f-8ed9-8c252dd99873" src="https://github.com/user-attachments/assets/a44e8fee-d724-49cc-8248-adf46f699643" />

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
<img width="839" height="72" alt="437522071-bc055139-9155-41b5-a25f-8ba5e785fda1" src="https://github.com/user-attachments/assets/5a4bb929-9848-40ad-b5c9-9ff433274430" />


# RESULT:
The Commands are executed successfully.
