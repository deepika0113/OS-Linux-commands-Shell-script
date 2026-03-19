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
<img width="436" height="152" alt="image" src="https://github.com/user-attachments/assets/3faf7f8d-5f5a-49e0-98e5-8742d818e64b" />


cat < file2
## OUTPUT
<img width="483" height="146" alt="image" src="https://github.com/user-attachments/assets/f7539e00-367a-4149-9a16-a66de20d1f09" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="526" height="68" alt="image" src="https://github.com/user-attachments/assets/3d36d572-a19a-4535-806f-b07c2d2e064f" />


comm file1 file2
 ## OUTPUT
<img width="597" height="225" alt="image" src="https://github.com/user-attachments/assets/b7b76a9e-25f5-434c-98b7-7b34ae7450ff" />


 
diff file1 file2
## OUTPUT
<img width="493" height="301" alt="image" src="https://github.com/user-attachments/assets/0afe0faa-69b5-4422-ae5e-9dbb00b38f95" />



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

<img width="374" height="93" alt="image" src="https://github.com/user-attachments/assets/2bde9012-7502-4f77-953d-4e7632ddf20a" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="428" height="129" alt="image" src="https://github.com/user-attachments/assets/d69bea22-ec0c-440f-b5a1-45b84ea1f253" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="428" height="123" alt="image" src="https://github.com/user-attachments/assets/99838126-3f78-4f49-b092-d8a11fe4a7c4" />



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

<img width="330" height="74" alt="image" src="https://github.com/user-attachments/assets/ffe1f0be-4848-4d9b-bdf8-ecffe24ebff7" />



grep hello newfile 
## OUTPUT

<img width="414" height="76" alt="image" src="https://github.com/user-attachments/assets/0ac9c02b-9847-4dd2-9eef-273b2f5185c1" />




grep -v hello newfile 
## OUTPUT

<img width="451" height="98" alt="image" src="https://github.com/user-attachments/assets/27f5723a-7379-4c63-a193-c2decd448d7c" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="445" height="82" alt="image" src="https://github.com/user-attachments/assets/10a0347c-962b-46e1-809b-1e7bb351230e" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="531" height="80" alt="image" src="https://github.com/user-attachments/assets/b2a13cab-9b65-4aea-a69c-025eb6a210a2" />



grep -R ubuntu /etc
## OUTPUT

<img width="1283" height="580" alt="image" src="https://github.com/user-attachments/assets/d70a3ee1-b652-426a-bb3c-4455bbc225ef" />



grep -w -n world newfile   
## OUTPUT
<img width="465" height="95" alt="image" src="https://github.com/user-attachments/assets/717d291e-d50c-4275-aaa9-faff40f2fa08" />



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

<img width="439" height="99" alt="image" src="https://github.com/user-attachments/assets/da1a9e69-a0d9-4fcd-9e60-c297b3668f95" />



egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="515" height="105" alt="image" src="https://github.com/user-attachments/assets/d6970806-1880-4a3a-88f4-fdd5f999eda7" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="437" height="73" alt="image" src="https://github.com/user-attachments/assets/5926fa31-3eaa-40e1-aad4-ee15bbc53fd7" />



egrep '(world$)' newfile 
## OUTPUT

<img width="472" height="104" alt="image" src="https://github.com/user-attachments/assets/a480ce39-b943-4dc3-9ffa-87da104ea773" />



egrep '(World$)' newfile 
## OUTPUT



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="441" height="129" alt="image" src="https://github.com/user-attachments/assets/ad8f4b10-ecb4-42c3-9bfa-940d3a9a5b1e" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="429" height="76" alt="image" src="https://github.com/user-attachments/assets/6af06800-0422-4f91-bfac-d45aac90f011" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="416" height="75" alt="image" src="https://github.com/user-attachments/assets/8af3927e-f58c-48b2-be11-e805340517ff" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="417" height="73" alt="image" src="https://github.com/user-attachments/assets/c07eb1d2-459e-4d92-b790-026448a97bc7" />



egrep l{2} newfile
## OUTPUT
<img width="435" height="102" alt="image" src="https://github.com/user-attachments/assets/f3a77366-93c0-4e57-853f-58279719fafb" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="450" height="125" alt="image" src="https://github.com/user-attachments/assets/17fa0893-6e1a-4733-ae37-9ec5806a652b" />



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
<img width="358" height="80" alt="image" src="https://github.com/user-attachments/assets/b6dbeedd-2729-4c82-9dd3-f07f278d00b9" />




sed -n -e '$p' file23
## OUTPUT
<img width="346" height="76" alt="image" src="https://github.com/user-attachments/assets/c6ec23a6-7c0d-460d-b59e-3b1cef2e3108" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="508" height="250" alt="image" src="https://github.com/user-attachments/assets/1ae24715-32b9-4222-bce8-b3cc102f7eeb" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="507" height="255" alt="image" src="https://github.com/user-attachments/assets/cbddf18a-088a-4802-bf18-89cd4ffc36cf" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="562" height="251" alt="image" src="https://github.com/user-attachments/assets/599cf310-abd9-403b-bd2c-bf633987db13" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="578" height="171" alt="image" src="https://github.com/user-attachments/assets/32277641-2b86-479e-8f0d-37ae92d37fa1" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="475" height="123" alt="image" src="https://github.com/user-attachments/assets/7cdb6e61-fd21-4be0-9e9c-9a8c770bf8c1" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="446" height="110" alt="image" src="https://github.com/user-attachments/assets/3f840b4e-50f3-4f6e-bb9d-24744954a32a" />




seq 10 
## OUTPUT

<img width="401" height="304" alt="image" src="https://github.com/user-attachments/assets/30dea5cd-ed33-4175-85a7-1c9b4a612f82" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="425" height="127" alt="image" src="https://github.com/user-attachments/assets/d830b986-c967-4c97-8e71-897a77c4bc30" />




seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="420" height="126" alt="image" src="https://github.com/user-attachments/assets/deeb21d7-2789-4cb2-ba96-1cf4af59c7df" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="387" height="151" alt="image" src="https://github.com/user-attachments/assets/8adcafbf-9217-4094-b876-e42b16043d6b" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="400" height="134" alt="image" src="https://github.com/user-attachments/assets/bc9ee4e6-8a8b-4244-88bd-f7dea4af321e" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="465" height="130" alt="image" src="https://github.com/user-attachments/assets/0b536f76-714b-4e78-b4c8-ba38975bf42c" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="568" height="126" alt="image" src="https://github.com/user-attachments/assets/cfff21fa-a5ab-442b-88ad-4bbde4af83fb" />



sed -n '2,4{s/$/*/;p}' file23
<img width="473" height="130" alt="image" src="https://github.com/user-attachments/assets/74afbdc4-0a82-4f1b-ba0f-af7c25de087e" />



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
<img width="462" height="178" alt="image" src="https://github.com/user-attachments/assets/9b69fba0-4a74-4460-bd66-6ca5daa4a6a1" />



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
<img width="437" height="177" alt="image" src="https://github.com/user-attachments/assets/b367ea9e-b8f0-4da0-9828-05953b5e5f0b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="687" height="269" alt="image" src="https://github.com/user-attachments/assets/f9512bce-10a4-4a75-bc57-8a346cb2b3ea" />



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
<img width="442" height="120" alt="image" src="https://github.com/user-attachments/assets/79137006-cb8a-4c96-b6b6-b2f430f49ab8" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="561" height="130" alt="image" src="https://github.com/user-attachments/assets/2910b885-1ba7-46de-abd5-45892761592e" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="727" height="780" alt="image" src="https://github.com/user-attachments/assets/b3f69b6f-45c5-4712-b737-b1af7ad9b8e6" />

<img width="722" height="745" alt="image" src="https://github.com/user-attachments/assets/a6457178-2ac6-4d12-ae1c-6539f69e6c56" />

<img width="692" height="720" alt="image" src="https://github.com/user-attachments/assets/bb5ce89d-4909-4df0-ae52-c05e6b7aa40b" />

<img width="707" height="774" alt="image" src="https://github.com/user-attachments/assets/8a69066f-9c7c-436b-8593-3db2996cd828" />

<img width="727" height="776" alt="image" src="https://github.com/user-attachments/assets/6cd13094-fb71-4564-8d90-fcacdaf5bee3" />



](<img/ss48 d.png>)
mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="732" height="697" alt="image" src="https://github.com/user-attachments/assets/37eb7c50-d9b6-4a2b-bc98-82c557a7a787" />

<img width="744" height="737" alt="image" src="https://github.com/user-attachments/assets/806b9a26-a304-4ebb-b8de-2428f8f3b38f" />



tar -xvf backup.tar
## OUTPUT
<img width="621" height="768" alt="image" src="https://github.com/user-attachments/assets/5ea56801-592c-44ba-a995-30fd444134ea" />

<img width="720" height="775" alt="image" src="https://github.com/user-attachments/assets/a746968d-a933-4f83-8573-f4552e66c217" />

<img width="663" height="742" alt="image" src="https://github.com/user-attachments/assets/7aa63e7f-f039-4ff3-9943-21ae65ace634" />

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
<img width="413" height="134" alt="image" src="https://github.com/user-attachments/assets/b03912d1-43ab-452c-a7cc-fcae5c16cd71" />



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
<img width="685" height="398" alt="image" src="https://github.com/user-attachments/assets/0c932a44-9049-44b7-9044-68f627ea3077" />


 
ls file1
## OUTPUT
<img width="362" height="80" alt="image" src="https://github.com/user-attachments/assets/e707f21f-8cd1-4b3d-8caa-6280781b6e12" />


echo $?
## OUTPUT 
<img width="336" height="84" alt="image" src="https://github.com/user-attachments/assets/6ffd5c21-dfed-49c7-937b-2830dfee1568" />


./one
bash: ./one: Permission denied

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
<img width="501" height="256" alt="image" src="https://github.com/user-attachments/assets/2acf6c03-f617-409d-99a3-76fd39b9d9b3" />





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
# output
<img width="655" height="103" alt="image" src="https://github.com/user-attachments/assets/bf0147d8-8f32-4ccf-81d5-07d47e059ada" />


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
<img width="647" height="129" alt="image" src="https://github.com/user-attachments/assets/4e598ebe-fc81-4227-b53a-5c83d12a6f5a" />

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
<img width="655" height="103" alt="image" src="https://github.com/user-attachments/assets/0d28592d-aaaa-4d9b-8e3a-c6d607cf3f13" />


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
<img width="676" height="111" alt="image" src="https://github.com/user-attachments/assets/dd496a85-dd58-4ca7-a2dd-c29817f0ce72" />


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
<img width="493" height="80" alt="image" src="https://github.com/user-attachments/assets/adc418e0-c038-48bf-b0d1-ce61140d5a83" />


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
 
![ss67](https://github.com/user-attachments/assets/8cb06f8a-2bc0-4bd1-8045-2ee37c517a92)

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```


 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```

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
<img width="667" height="183" alt="image" src="https://github.com/user-attachments/assets/7bb2b20e-faa6-4b7b-8032-628a6936e60d" />

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
<img width="440" height="358" alt="image" src="https://github.com/user-attachments/assets/9b99e14c-f0c8-47ca-91a1-2b4cb5636891" />


 
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
<img width="699" height="125" alt="image" src="https://github.com/user-attachments/assets/5b3a4d5f-862a-40e8-9bc9-0209f295a9e1" />

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
<img width="633" height="156" alt="image" src="https://github.com/user-attachments/assets/eb052d42-44ea-44f3-8eff-7ee34e1dbc08" />


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
<img width="405" height="106" alt="image" src="https://github.com/user-attachments/assets/413d589f-b00a-4569-a6b7-596ed9a3bd60" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="494" height="70" alt="image" src="https://github.com/user-attachments/assets/7783fd78-50a1-4018-a4d7-8d4b92ff9203" />




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
<img width="405" height="81" alt="image" src="https://github.com/user-attachments/assets/c0fbdbf4-0388-405e-83ca-2b5df1148e2b" />



 
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
<img width="427" height="129" alt="image" src="https://github.com/user-attachments/assets/5c6b9cdf-6219-471c-986f-0ddc3a3431fb" />

 
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
<img width="385" height="376" alt="image" src="https://github.com/user-attachments/assets/0c406f31-f3fe-4f95-bfbc-d3f426c4cd69" />

 
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
<img width="372" height="129" alt="image" src="https://github.com/user-attachments/assets/5bed6cf2-c137-4401-8f0d-908d34566ccf" />



# RESULT:
The Commands are executed successfully.
