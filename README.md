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
<img width="274" height="141" alt="image" src="https://github.com/user-attachments/assets/be918067-0ec2-4336-8256-6440ecb7fda2" />

cat < file2
## OUTPUT
<img width="317" height="144" alt="image" src="https://github.com/user-attachments/assets/f875be38-89d5-4c94-8720-5218718b55c4" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="380" height="68" alt="image" src="https://github.com/user-attachments/assets/ad0c2487-f1f7-462e-ab4b-03ff1905d059" />

comm file1 file2
 ## OUTPUT
<img width="391" height="215" alt="image" src="https://github.com/user-attachments/assets/0c2c5c2a-e369-4041-a8ac-3f4c46328611" />

 
diff file1 file2
## OUTPUT


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
<img width="283" height="95" alt="image" src="https://github.com/user-attachments/assets/de0e22b5-29c4-4200-ab30-cebf1e741102" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="310" height="119" alt="image" src="https://github.com/user-attachments/assets/9fd7b66d-18f5-423f-803b-845e1dc6aafe" />


cut -d "|" -f 2 file22
## OUTPUT


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
<img width="331" height="65" alt="image" src="https://github.com/user-attachments/assets/df7cede5-f62a-4388-93ff-f8e323b8334d" />



grep hello newfile 
## OUTPUT

<img width="330" height="73" alt="image" src="https://github.com/user-attachments/assets/597253a6-1ba8-4dab-a6aa-1ecf2ad5b94f" />



grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT

<img width="368" height="95" alt="image" src="https://github.com/user-attachments/assets/9000977d-dd48-4920-b592-8c419b0ef48b" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="405" height="70" alt="image" src="https://github.com/user-attachments/assets/80a31a98-5d5e-45bd-809d-c791c4a133fc" />




grep -R ubuntu /etc
## OUTPUT
<img width="326" height="45" alt="image" src="https://github.com/user-attachments/assets/de74d3ed-defa-441a-b67a-85f10c63717a" />



grep -w -n world newfile   
## OUTPUT
<img width="326" height="97" alt="image" src="https://github.com/user-attachments/assets/57b8eb02-9e5c-444f-b382-dc199f9975f3" />


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

<img width="401" height="107" alt="image" src="https://github.com/user-attachments/assets/39f0f87e-c046-4726-bcab-38c42f8f4adb" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="365" height="99" alt="image" src="https://github.com/user-attachments/assets/88a2ed6e-458c-4734-8ad0-6bcfaf5a7ac8" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="421" height="103" alt="image" src="https://github.com/user-attachments/assets/8ee765af-670b-4a15-b367-22c734400eb8" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="328" height="75" alt="image" src="https://github.com/user-attachments/assets/52601d78-16c2-42ad-aa75-dfe7295d3694" />

egrep '(world$)' newfile 
## OUTPUT
<img width="327" height="101" alt="image" src="https://github.com/user-attachments/assets/5a97146b-8cd7-4026-88e5-e828758cc24c" />



egrep '(World$)' newfile 
## OUTPUT
<img width="354" height="65" alt="image" src="https://github.com/user-attachments/assets/a29cdd07-323a-409f-afe5-e8db7a1d4ba9" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="409" height="120" alt="image" src="https://github.com/user-attachments/assets/e2136dc2-729f-4c92-8927-e08da8fbf9d8" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="334" height="75" alt="image" src="https://github.com/user-attachments/assets/d22024a1-615f-4528-ba5a-709dda7e68f9" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="388" height="78" alt="image" src="https://github.com/user-attachments/assets/81865bdc-a67e-4685-8155-78b2870b442a" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="412" height="74" alt="image" src="https://github.com/user-attachments/assets/ea00f7a9-f5ef-49bd-9593-dd17babcb437" />


egrep l{2} newfile
## OUTPUT
<img width="302" height="96" alt="image" src="https://github.com/user-attachments/assets/2f2831f2-d75e-4a8d-a67d-d3b5594c3eb3" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="295" height="132" alt="image" src="https://github.com/user-attachments/assets/7bd504af-ba1c-4606-b257-f2a847848000" />

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

<img width="339" height="80" alt="image" src="https://github.com/user-attachments/assets/72d49f20-096a-4f96-82ad-6c0f68b5be15" />


sed -n -e '$p' file23
## OUTPUT


<img width="312" height="73" alt="image" src="https://github.com/user-attachments/assets/4062e4a8-8596-4263-9455-409329425bb2" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="360" height="271" alt="image" src="https://github.com/user-attachments/assets/a32de008-1d47-4b68-9c7d-c691cd0177a8" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="378" height="275" alt="image" src="https://github.com/user-attachments/assets/d2ccbfe8-984c-4276-8260-ec9b3748748a" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="341" height="170" alt="image" src="https://github.com/user-attachments/assets/2264447f-48f8-4d34-8b6f-ad64056cc32e" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="380" height="119" alt="image" src="https://github.com/user-attachments/assets/9ccbe5d6-8a06-40e8-abc4-2936c6e0ab84" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



seq 10 
## OUTPUT
<img width="298" height="299" alt="image" src="https://github.com/user-attachments/assets/62843a97-ff40-4ddc-b71d-33dd23faf294" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="294" height="121" alt="image" src="https://github.com/user-attachments/assets/0861fdf6-6e39-47c0-ad55-52719abe416d" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="326" height="109" alt="image" src="https://github.com/user-attachments/assets/f35a4c7e-43c3-46c4-8963-92f869d25f2a" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="310" height="146" alt="image" src="https://github.com/user-attachments/assets/3255169e-792a-4227-94b1-95929c293b12" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="300" height="127" alt="image" src="https://github.com/user-attachments/assets/6d0a45aa-0aa2-4834-a2fb-6d4a05a02853" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="341" height="115" alt="image" src="https://github.com/user-attachments/assets/aff42699-2cf9-41bd-8c62-66cb1881a088" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="380" height="126" alt="image" src="https://github.com/user-attachments/assets/46cddb94-6358-46b2-8c68-6949b1c62d7f" />


sed -n '2,4{s/$/*/;p}' file23

<img width="361" height="117" alt="image" src="https://github.com/user-attachments/assets/949a3614-4a0c-4c36-b4a0-d7aedf45bcc5" />

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
<img width="380" height="199" alt="image" src="https://github.com/user-attachments/assets/2c160de4-133d-4a77-a887-f9388693b83f" />


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
<img width="316" height="175" alt="image" src="https://github.com/user-attachments/assets/daf8735d-bb81-40d7-a033-8b0822a84b97" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="441" height="281" alt="image" src="https://github.com/user-attachments/assets/b7f6201e-4d0d-4f25-acbf-41a69deff47a" />

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

<img width="348" height="117" alt="image" src="https://github.com/user-attachments/assets/3882fcfb-1031-4c96-b5a7-aac5a38433aa" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="476" height="120" alt="image" src="https://github.com/user-attachments/assets/3de16f9c-d36c-4885-bf13-1bd4cdf2523b" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="749" height="490" alt="image" src="https://github.com/user-attachments/assets/dd488122-17a7-47e2-bd9a-ad82482fca7a" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="749" height="490" alt="image" src="https://github.com/user-attachments/assets/df2b81ff-cedf-4863-9b04-7d23cde90c7e" />

tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
<img width="530" height="79" alt="image" src="https://github.com/user-attachments/assets/55c1765c-2df6-44f4-abd5-ad6164e809d9" />

gunzip backup.tar.gz
## OUTPUT
<img width="355" height="36" alt="image" src="https://github.com/user-attachments/assets/7f75605d-0510-4da8-a9ba-85bf0c15b179" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="435" height="118" alt="image" src="https://github.com/user-attachments/assets/5e1a5ff8-44ca-4957-996f-edf7c4e736ca" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="321" height="127" alt="image" src="https://github.com/user-attachments/assets/fb636a82-35fe-4780-ad58-097f248bca91" />


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
<img width="649" height="290" alt="image" src="https://github.com/user-attachments/assets/9e04cd27-a605-445b-8ab9-45ffe9d6f25a" />

 
ls file1
## OUTPUT
<img width="310" height="89" alt="image" src="https://github.com/user-attachments/assets/f2f9b2ae-250e-4bf0-bd14-756b078f18fe" />

echo $?
## OUTPUT 
<img width="287" height="71" alt="image" src="https://github.com/user-attachments/assets/267fde79-81ac-48e3-8359-5fbd75135d49" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

<img width="287" height="71" alt="image" src="https://github.com/user-attachments/assets/84864506-6954-43c2-9a0c-10b1735e498b" />

 
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

<img width="360" height="274" alt="image" src="https://github.com/user-attachments/assets/b58d418e-20e4-4d3e-a234-4552f754a27b" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="621" height="160" alt="image" src="https://github.com/user-attachments/assets/67777db6-671f-4135-9eda-ce8ad0acd6a4" />


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
<img width="428" height="65" alt="image" src="https://github.com/user-attachments/assets/ad85cdcf-faf4-451c-808b-69b90a112abb" />

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

<img width="426" height="66" alt="image" src="https://github.com/user-attachments/assets/56c0c157-0e35-46f8-922f-303481ec1708" />



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
<img width="426" height="66" alt="image" src="https://github.com/user-attachments/assets/4e1bb4d7-fae2-4731-9d93-0c001a00fb53" />

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
<img width="693" height="102" alt="image" src="https://github.com/user-attachments/assets/db77c59c-907e-4169-83b2-e9fe77dc0c79" />

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
 ##OUTPUT:
 <img width="362" height="67" alt="image" src="https://github.com/user-attachments/assets/d606419f-3958-41e3-be43-75cd69904916" />

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
 <img width="635" height="151" alt="image" src="https://github.com/user-attachments/assets/8da07b15-65fa-4134-abf6-a82c671baac1" />

 
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
 
 ##OUTPUT:
 <img width="564" height="218" alt="image" src="https://github.com/user-attachments/assets/311b70e7-df6b-42aa-813d-f4ee7e43f864" />

 
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
 OUTPUT:
 <img width="620" height="240" alt="image" src="https://github.com/user-attachments/assets/43910e13-57de-4043-95e3-9a059b9abae6" />

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
 OUTPUT:
 <img width="641" height="224" alt="image" src="https://github.com/user-attachments/assets/31bcc668-69e9-4361-914d-b4fa58d4d309" />

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
 OUTPUT:
 <img width="660" height="292" alt="image" src="https://github.com/user-attachments/assets/45fdd349-f028-4e08-beb7-2de6df0535d4" />

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
<img width="561" height="135" alt="image" src="https://github.com/user-attachments/assets/5d0da5e3-a6a8-4741-85ff-f49c529ac676" />

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="561" height="135" alt="image" src="https://github.com/user-attachments/assets/bf20cb1b-f24a-4bf0-a04e-e80c9802908d" />

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
<img width="309" height="221" alt="image" src="https://github.com/user-attachments/assets/b8b414fb-c16e-48a0-81b5-b1fb35523793" />

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
<img width="332" height="225" alt="image" src="https://github.com/user-attachments/assets/e1cbb68e-21c6-4a9b-9c48-2d02c9387501" />

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

 <img width="350" height="400" alt="image" src="https://github.com/user-attachments/assets/0f1da485-8d56-4590-86ab-c0acc018cc0e" />

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
<img width="585" height="203" alt="image" src="https://github.com/user-attachments/assets/90f8ec5a-3cba-4545-8207-9462c0ae4055" />
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
 <img width="355" height="229" alt="image" src="https://github.com/user-attachments/assets/cbe334a8-d8fb-483a-9119-25f141d6160d" />

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
<img width="455" height="143" alt="image" src="https://github.com/user-attachments/assets/70afbc72-78c5-4cf0-8576-16bf5a1c3366" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="325" height="161" alt="image" src="https://github.com/user-attachments/assets/080ea3ed-3e77-4d02-9a61-c946e023c8d3" />



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
<img width="351" height="165" alt="image" src="https://github.com/user-attachments/assets/1c1730ba-d525-40a8-9490-7ce2636813f8" />

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
 <img width="351" height="165" alt="image" src="https://github.com/user-attachments/assets/0975aa2e-7cfd-4e79-9457-a6fad2c1063d" />

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
 <img width="351" height="165" alt="image" src="https://github.com/user-attachments/assets/444b8869-f540-47d2-b153-2715098c9e4f" />

 
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
## OUTPUT :

<img width="642" height="204" alt="Screenshot 2025-09-23 104004" src="https://github.com/user-attachments/assets/86d9d589-a9ee-43e1-ba0f-c80d606fbea2" />


# RESULT:
The Commands are executed successfully.
