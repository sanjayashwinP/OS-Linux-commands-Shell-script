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

chanchal singhvi     
c.k. shukla    
s.n. dasgupta    
sumit chakrobarty    
^d   

cat < file2
## OUTPUT

anil aggarwal    
barun sengupta    
c.k. shukla     
lalit chowdury   
s.n. dasgupta   
^d   
# Comparing Files
cmp file1 file2
## OUTPUT
 ![305638280-75a5512e-1a3b-45f7-ad9a-369f872d4e8a](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/4ec306f9-494f-4dc0-8c27-1c8d3e5ff722)

comm file1 file2
 ## OUTPUT
![305638353-06aaf5ba-ea64-4e0c-8499-115f566e830f](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/4009da47-8f06-4b1e-8ed0-c9d5a994591c)

 
diff file1 file2
## OUTPUT
![305638538-dd5d576c-fdad-4142-8a42-957143d516bb](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/89c87c22-bf9b-41cf-88f0-48758aef4d25)



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
![305638593-057abf47-bdbc-4ed1-b8c0-df0302401aad](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/4a7bf6fb-9ff0-4a29-b000-2905a6684213)




cut -d "|" -f 1 file22
## OUTPUT

![305638603-64f3b346-85d6-40e6-a5ca-0795b38c67c2](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/934c48a1-b626-4f90-ae21-06d397283680)


cut -d "|" -f 2 file22
## OUTPUT

![305638740-26e24d41-1567-4bb7-a427-463ae5f32f95](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/82de70e6-e150-46f4-a595-b37313d08556)

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

![305638765-a75c35a9-3407-45bb-a60c-51ac39e93dd0](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/a96c3188-864e-4e74-b63d-f805662f22e8)


grep hello newfile 
## OUTPUT
![305638777-1fed07d9-9937-4958-934c-dae3f0c403d3](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/cd63b2cb-2fcd-4170-b658-93e3659e6ad1)




grep -v hello newfile 
## OUTPUT

![305638788-675e0427-572c-4aca-953c-cc45455944ae](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/4701689d-e2a0-4c9b-8d5a-01670b06e74e)


cat newfile | grep -i "hello"
## OUTPUT

![305638803-8dea6fe3-2ada-4ab9-ae14-db1f7eaa36f7](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/0c515140-2e01-44f8-bfbd-0b767f25e4b8)



cat newfile | grep -i -c "hello"
## OUTPUT


![305638905-fd4ce646-de28-4957-83b6-e305c1f4439a](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/2f3d125a-41b7-4be0-af35-08806d24ada6)


grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

![305638979-dfaf1853-3e52-470b-9bc5-38d3057ce4b2](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/8c1a9c02-136c-464c-be5a-ecd6b9c16b96)

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

![305638995-63f44836-f6b6-4d66-bdf4-9a53fb6fe0d4](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/b6dbb2cd-893a-42da-b539-bee7b86e946e)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![305639002-8cc574fc-24a7-4e1d-bfd0-56ca0ff8dd45](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/64407afe-4dae-4cc0-a2dc-90e7c978099f)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![305639007-50e2bb9b-2c9b-4df4-9d46-903adbd0e6da](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/5e508e89-13f0-47f2-b071-b9dc2613cfd1)


egrep '(^hello)' newfile 
## OUTPUT
![305639010-67ad9538-9b91-423e-8266-1fb2edbc9d40](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/0cd8839e-6ffd-4839-80b4-71193fd4cf04)



egrep '(world$)' newfile 
## OUTPUT


![305639019-6339ba41-1e5e-443d-825d-b2809e856a19](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/aeb19ded-2f21-4b53-8eed-7c07003930de)

egrep '(World$)' newfile 
## OUTPUT
![305639035-fb6711f3-9556-4718-a749-555f06debab1](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/e7cbdaaf-2927-4686-b403-521d08fe141a)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![305639048-cc9d61d6-82b4-42a2-a3eb-593038c19fc7](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/020794be-8897-46f8-8952-cc78bd925fa2)


egrep '[1-9]' newfile 
## OUTPUT
![305639050-6d099778-2b88-4e6f-8b06-c40b2f09a638](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/3281acde-abd4-4057-9e29-4e00908add55)



egrep 'Linux.*world' newfile 
## OUTPUT
![305639093-d1c365df-03a4-4e54-928e-4a381e058096](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/5ddc5891-f795-40e1-950d-44624ff7d8a0)


egrep 'Linux.*World' newfile 
## OUTPUT

![305639103-591ab9e6-e543-40a3-a4ec-f9012f8ceadf](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/64a2a04d-b60c-4008-b915-32170088b56a)

egrep l{2} newfile
## OUTPUT

![305639113-98619322-54a4-4a4c-ad34-fa84af7dfff4](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/e64cafbc-a423-47a3-899b-9778dd2a7759)


egrep 's{1,2}' newfile
## OUTPUT 

![305639119-91245c5a-f669-4b1c-8641-44667f0689f7](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/ddc3d485-3124-4a30-8d05-805087d8f281)

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

![305639126-6067006c-52ab-4263-bb7c-8675a5cba9d7](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/2b923f83-5eef-4756-9c87-7cba306724b1)


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![305639157-ea154aa6-2031-4bc9-a5fa-d246da2078ce](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/ffae312a-ab4e-4f8c-8270-31b9679d3883)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![305639166-b35d81b6-ed9b-4d25-b8cb-d3ca5c25fdf0](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/013164f4-f3f4-4447-88cd-2d120772f1fe)




sed  '/tom/s/5000/6000/' file23
## OUTPUT


![305639177-e6e1ba26-5291-43fd-8f40-d6fe00a20498](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/ff53fc87-f67c-4d98-aa90-b6b22d6a9d2d)

sed -n -e '1,5p' file23
## OUTPUT
![305639187-d727de65-8c1f-474b-a1a7-2d87bbc4b354](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/d9ba3869-7394-4b1a-b0d1-14ebe3f33355)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![305639194-ca6da655-591e-498b-9afb-e9bcd8e09c64](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/3eb3b618-0db1-47af-94ea-b92e76516595)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![305639202-7a82bd4e-4d0e-4340-89d1-882aa938ae94](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/c4380816-be70-4050-9d02-0c07ea577809)



seq 10 
## OUTPUT

![305639219-fa19b57d-1c9d-4bef-81a8-159ef1e802be](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/707a62c8-cbc8-48c1-b6b9-c252b33a153c)


seq 10 | sed -n '4,6p'
## OUTPUT

![305639234-a4650fd0-7816-4e90-88fe-036a692d2e76](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/8cb265d2-6e6a-4678-91dd-aca82f6a5f32)


seq 10 | sed -n '2,~4p'
## OUTPUT
![305639247-e76d46db-4e87-4616-adf3-209f22705a28](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/a1e5813e-b365-4b27-9420-b91dd40dd444)



seq 3 | sed '2a hello'
## OUTPUT
![305639257-b251a39b-a769-44e6-aca2-a4a33e8afc48](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/f4726314-c5e6-4070-ae91-5ccacd81b998)



seq 2 | sed '2i hello'
## OUTPUT
![305639297-50840e06-7531-454b-893b-82157fa696d9](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/e17391bc-bbfd-4ce0-9481-d6624a2feff9)


seq 10 | sed '2,9c hello'
## OUTPUT

![305639305-02460176-5dbc-4cd3-86e2-676ef79130bc](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/09bf3d50-72b5-422a-aaae-876796b840bb)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![305639312-757e595f-068c-4a2d-9a74-a0c5c280d674](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/8da64af4-8eaf-4055-9631-c67efd896f70)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![305639376-3a948998-5ccc-471c-8301-871e4f040ac5](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/2726bb0a-9852-4a80-8f0a-8985f0b03f1e)

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
![305639387-9dcd56c0-8260-4a34-a658-4a9bedfc00a6](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/f56b0e3c-b7f3-4082-9736-a16ced1f44db)


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

![305639402-10564297-a8ca-42e7-9e7b-11d2f5823b34](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/bce4c066-884c-494d-ba9c-a86b1394ede4)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![305639440-9ddada14-d8d3-4b5a-a383-4e756bac6c9c](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/266cd28c-1ccd-4cb2-9bad-94abd6d264c2)

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
![305639452-a3958730-a84b-4be3-934c-75127fd45e20](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/162a880b-5a2f-40ea-ad2c-fc512565c3fe)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![305639476-36ba05c2-828f-4cf0-b89c-7704eb2a9ca0](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/27d2df3b-3fd0-4ead-baf6-c5c6d3f2e1c9)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![305639489-59aebb74-5bab-4b16-856c-0702c0987aa0](https://github.com/sanjayashwinP/OS-Linux-commands-Shell-script/assets/147473265/e842c0c8-c7ab-4634-b3ff-712f0240370c)


mkdir backupdir
 
mv backup.tar backupdir
 
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
