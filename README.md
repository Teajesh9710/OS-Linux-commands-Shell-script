cd# OS-Linux-commands-Shell-scripting
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
<img width="370" height="139" alt="image" src="https://github.com/user-attachments/assets/e5272a1b-dea0-441d-b0fb-e0f9b7d10788" />



cat < file2
## OUTPUT
<img width="411" height="187" alt="image" src="https://github.com/user-attachments/assets/9165b71f-14ae-4bbe-965d-bd9d4fe3e84b" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="552" height="89" alt="image" src="https://github.com/user-attachments/assets/87795559-835d-4c8d-941f-59311f6e8fbe" />

comm file1 file2
 ## OUTPUT
<img width="524" height="224" alt="image" src="https://github.com/user-attachments/assets/d67d8ae8-21e6-4872-b39b-799387e0e09a" />

 
diff file1 file2
## OUTPUT
<img width="557" height="280" alt="image" src="https://github.com/user-attachments/assets/e5120b01-b956-4ca5-a83e-0d94752be39a" />


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

<img width="470" height="102" alt="image" src="https://github.com/user-attachments/assets/7e653cd4-b062-4657-a05f-179b662cbcc6" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="494" height="145" alt="image" src="https://github.com/user-attachments/assets/d5094891-8a73-492d-bf7d-c69babb25fac" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="548" height="135" alt="image" src="https://github.com/user-attachments/assets/3ae7a9ba-5d7f-4f3a-bf39-a6611d164435" />


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
<img width="425" height="90" alt="image" src="https://github.com/user-attachments/assets/25fa07e3-aca6-487f-be5e-c5e391da2f14" />



grep hello newfile 
## OUTPUT

<img width="625" height="117" alt="image" src="https://github.com/user-attachments/assets/1409f7d2-9d19-4e0e-86b4-4b8beeaf9101" />



grep -v hello newfile 
## OUTPUT

<img width="475" height="87" alt="image" src="https://github.com/user-attachments/assets/b253fcf0-8a9a-48ba-a195-f8c04c67ae45" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="493" height="92" alt="image" src="https://github.com/user-attachments/assets/768b90c8-69c0-41ef-a21d-5c0a9120d525" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="476" height="89" alt="image" src="https://github.com/user-attachments/assets/f3a9f266-0c01-4483-930f-7ddb36eba060" />



grep -w -n world newfile   
## OUTPUT

<img width="527" height="72" alt="image" src="https://github.com/user-attachments/assets/48abd272-1e70-4c8f-9c82-6b80b49e2e65" />

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
<img width="497" height="97" alt="image" src="https://github.com/user-attachments/assets/c6cc4b09-6b31-4017-9160-2e5851a38a1e" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="554" height="103" alt="image" src="https://github.com/user-attachments/assets/8124af48-f5f4-45b1-8c20-e08cc3ef0fb0" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="549" height="117" alt="image" src="https://github.com/user-attachments/assets/ca7db36c-0b08-436a-9e26-6cde9ab36704" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="374" height="81" alt="image" src="https://github.com/user-attachments/assets/3ae2fcba-1671-424f-bee3-7dc631b14a3a" />



egrep '(world$)' newfile 
## OUTPUT
<img width="656" height="111" alt="image" src="https://github.com/user-attachments/assets/9baa1619-6d06-4e06-9af3-0ce7d958af9d" />



egrep '(World$)' newfile 
## OUTPUT
<img width="474" height="83" alt="image" src="https://github.com/user-attachments/assets/0de21d44-f6b1-48cc-bf16-332b2a622459" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="551" height="92" alt="image" src="https://github.com/user-attachments/assets/2ec1e63f-6a97-4f9f-a580-0caa08c9fc96" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="497" height="72" alt="image" src="https://github.com/user-attachments/assets/64905ee2-303e-4844-a0d5-54568ca12f49" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="505" height="90" alt="image" src="https://github.com/user-attachments/assets/d52c0c51-e0b2-45aa-a122-3ec30561bf2b" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="642" height="80" alt="image" src="https://github.com/user-attachments/assets/ba686c1c-4a5c-4da2-b3cd-6d292308fb69" />


egrep l{2} newfile
## OUTPUT
<img width="509" height="95" alt="image" src="https://github.com/user-attachments/assets/bb885751-68ab-4e86-bab0-8b5a94e5bb35" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="525" height="135" alt="image" src="https://github.com/user-attachments/assets/343cc01f-dcc7-41f2-8266-8cf8870e004d" />


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
<img width="717" height="69" alt="image" src="https://github.com/user-attachments/assets/f314725c-d222-4daa-ba1f-cd29ed2d8135" />



sed -n -e '$p' file23
## OUTPUT
<img width="440" height="95" alt="image" src="https://github.com/user-attachments/assets/ce51dea5-ddda-408f-9a45-969ca4b82d20" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="564" height="243" alt="image" src="https://github.com/user-attachments/assets/0ef38b06-d495-49fb-aed0-ab30f4aa8456" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="592" height="253" alt="image" src="https://github.com/user-attachments/assets/2ca30c6d-b906-4385-8b95-31ddbf167ce0" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="549" height="270" alt="image" src="https://github.com/user-attachments/assets/cdedd0c7-c6de-48d5-915f-79575a75cbfb" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="505" height="178" alt="image" src="https://github.com/user-attachments/assets/63610399-afd6-47bb-b16d-2c1c401ae3f7" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="397" height="131" alt="image" src="https://github.com/user-attachments/assets/c16e4ad9-6616-49b9-8bbc-fca5d5a87d2d" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="503" height="93" alt="image" src="https://github.com/user-attachments/assets/d5b2be0c-7a39-46f5-a510-b039af1264a1" />



seq 10 
## OUTPUT
<img width="404" height="330" alt="image" src="https://github.com/user-attachments/assets/5d0b2886-4bf4-4238-97af-53752d025eb9" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="409" height="126" alt="image" src="https://github.com/user-attachments/assets/f757c85a-f2fa-4754-9735-e15708c70ea6" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="440" height="138" alt="image" src="https://github.com/user-attachments/assets/092ee9d6-7a61-4a26-9d2a-94495ad711d4" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="433" height="146" alt="image" src="https://github.com/user-attachments/assets/0197bf46-5eed-4d95-bee0-8a0902675b4a" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="371" height="124" alt="image" src="https://github.com/user-attachments/assets/d5b3be2c-eec2-4253-99ec-6c4259d51521" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="452" height="112" alt="image" src="https://github.com/user-attachments/assets/c1f9df35-9c3e-4919-b767-bb60b6c521da" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="468" height="143" alt="image" src="https://github.com/user-attachments/assets/41991acb-a323-42ad-af19-cf0ff2d31235" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="477" height="124" alt="image" src="https://github.com/user-attachments/assets/6a6420f7-5750-4ebb-9d13-17bce7b6e09f" />

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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
