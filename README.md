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
![369744527-597b5c89-22dd-46cf-96ce-ecb15c24a9c6](https://github.com/user-attachments/assets/241eb95d-e294-44f0-8222-16521aca1293)


cat < file2
## OUTPUT
![369744631-2084183a-7163-4b4a-89c7-f5443d80d3f6](https://github.com/user-attachments/assets/988f7953-221e-4c2c-bbce-8e41299a154f)


# Comparing Files
cmp file1 file2
## OUTPUT
![369744635-30952f01-d061-4b41-b386-cd27c26100bc](https://github.com/user-attachments/assets/b04399a0-c662-487f-8ea3-f147f3565130)


comm file1 file2
 ## OUTPUT
![369744647-cffffafc-6c67-4220-9d2c-0c45071b73ad](https://github.com/user-attachments/assets/3d89fb60-ba03-43b4-ac89-48f9622cbbab)

 
diff file1 file2
## OUTPUT
![369744651-202dfab6-21c5-4ebf-b938-066f997ab79d](https://github.com/user-attachments/assets/a2121037-018d-4d8e-ba36-70b689437621)


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
![369744658-b5ba31ef-bba4-47eb-a916-a8b7e9248454](https://github.com/user-attachments/assets/63d6ad18-5906-4116-8f62-c1ca3b5993ea)


cut -d "|" -f 1 file22
## OUTPUT
![369744677-2d7a13ff-329b-47b8-a8dd-7ccd7a831428](https://github.com/user-attachments/assets/1a30c582-1f4f-41f2-9b58-1de470baf2d5)


cut -d "|" -f 2 file22
## OUTPUT
![369744685-08dd95f9-6bc3-4623-a8af-2d893079e107](https://github.com/user-attachments/assets/701addbf-644b-424f-b127-183633b13114)


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
![369744706-80662f07-c619-4f97-8455-9cea5f2da9be](https://github.com/user-attachments/assets/5ff7a535-7f3f-419f-9102-86eb1011ff14)


grep hello newfile 
## OUTPUT
![369744712-fde8236b-0b9e-48ea-a6c6-eb182db33a5a](https://github.com/user-attachments/assets/1463ed4f-009a-4258-b571-6fad85f7d954)


grep -v hello newfile 
## OUTPUT
![369744720-9ffd04ec-3d11-4076-af66-f821194f43bb](https://github.com/user-attachments/assets/f77589b4-b33c-42c4-a51a-aac53a39760c)


cat newfile | grep -i "hello"
## OUTPUT
![369744811-d332fd2c-ab9c-4fc0-bdbd-ff7e3735ad77](https://github.com/user-attachments/assets/3da30ab6-6715-41e1-96bf-3e0b71ba7840)


cat newfile | grep -i -c "hello"
## OUTPUT
![369744813-d957b202-bf1e-41c0-9652-1e6885018593](https://github.com/user-attachments/assets/e84ecfae-dab6-4b1f-9acb-eb48949561ab)


grep -R ubuntu /etc
## OUTPUT
![369744840-e8d884d2-030a-49b1-9117-3ff160232b88](https://github.com/user-attachments/assets/b1c6b992-14bf-4f23-8a88-6065a189f09a)


grep -w -n world newfile   
## OUTPUT
![369744861-cb4d45d1-284d-4ee6-9bd9-2c8060b7b8cc](https://github.com/user-attachments/assets/5b1673f3-aba9-4316-8f45-1490cd4e2db8)


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
![369744882-978170df-b710-4204-9f97-2fe250582251](https://github.com/user-attachments/assets/89b6c1cd-e461-487b-b1a3-37f07a09ad44)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![369744883-cc743417-d07b-4313-829e-b3eb76ae4482](https://github.com/user-attachments/assets/f819dc4c-8f41-43a2-92e0-394a76d1f742)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![369744883-cc743417-d07b-4313-829e-b3eb76ae4482](https://github.com/user-attachments/assets/b82543b8-d1e9-432e-9808-4f8210c31f69)


egrep '(^hello)' newfile 
## OUTPUT
![369744891-384dc944-e14d-42ef-b9b8-ef102b149d1f](https://github.com/user-attachments/assets/947af3dc-493d-4d63-8107-3d39c5a4b1e5)


egrep '(world$)' newfile 
## OUTPUT
![369744905-7c7166db-367c-49da-91f5-a509697a3b8b](https://github.com/user-attachments/assets/7d15a806-a293-42ba-83fd-45766c96c8e0)


egrep '(World$)' newfile 
## OUTPUT
![369744905-7c7166db-367c-49da-91f5-a509697a3b8b](https://github.com/user-attachments/assets/0693304e-7ac4-4503-92f7-f65a86e7f9ba)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![369744938-76b4e121-a36e-4eae-b96d-b4256cdc8721](https://github.com/user-attachments/assets/ab99a970-5158-4398-abf2-95cc9ec78cdc)


egrep '[1-9]' newfile 
## OUTPUT
![369744957-e7a36e91-f8f6-4a15-9895-8a5e132de55b](https://github.com/user-attachments/assets/7f0ccc1e-e947-494a-be2f-1a5a36ce5732)


egrep 'Linux.*world' newfile 
## OUTPUT
![369744998-f7be7f9c-a16b-4bd5-b691-65ac8fc182dd](https://github.com/user-attachments/assets/1a104d28-cd02-42f4-a8b7-845e2333a837)


egrep 'Linux.*World' newfile 
## OUTPUT
![369745057-6b08a443-0bb7-404a-a5e6-77215d046a74](https://github.com/user-attachments/assets/734300b1-8bbb-49a6-b66e-2b09786d736d)


egrep l{2} newfile
## OUTPUT
![369745084-25fd9619-0034-489a-8072-20b1dc516309](https://github.com/user-attachments/assets/30700b90-e298-45c0-bb63-9fb5d1d6f128)


egrep 's{1,2}' newfile
## OUTPUT 
![369745095-41b8c77c-b941-4386-8cd9-d5f380caa5ca](https://github.com/user-attachments/assets/c85d442f-830e-4aa9-b8bc-5e9d18bd4278)



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
![369745110-c7bf3a5c-6f31-4396-af04-97f5bfa8b272](https://github.com/user-attachments/assets/338479f3-5829-4269-b932-dbf732a6e8fd)

sed -n -e '$p' file23
## OUTPUT
![369745131-088023b1-2de9-4784-a5e8-f68202871d20](https://github.com/user-attachments/assets/9525b4bd-6fa3-431d-8d87-4870e1066b93)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![369745242-785fea5f-89a5-4170-84bc-653d92d43d85](https://github.com/user-attachments/assets/78b3aef9-f3fd-402e-9d34-4a0b38a9b68c)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![369745321-f4370443-5e37-401e-950a-ab32c546a4f9](https://github.com/user-attachments/assets/4dff7bd4-3c6c-4993-a861-950611dc47c8)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![369745334-ca1ccd7b-4db9-421d-83cf-ce8d2cab658a](https://github.com/user-attachments/assets/ef9484df-cd30-4244-9b16-09fc5b547013)

sed -n -e '1,5p' file23
## OUTPUT
![369745341-ccc5c432-54bc-4a03-a476-ae8edfb6c31b](https://github.com/user-attachments/assets/da8e9cd0-f155-4704-9023-cb2cc9d56ba8)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![369745360-be60705c-2d15-43d5-a19b-32a7296ff6dd](https://github.com/user-attachments/assets/3edb5972-ff4f-4678-b096-32efe1c713ac)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![369745370-e8201c8f-16df-404e-bfdb-9505cdab0ea8](https://github.com/user-attachments/assets/5e33e357-5008-4689-af40-941efcb9ba13)


seq 10 
## OUTPUT
![369745382-a4c542d7-0f46-4d6a-b4f6-be62dbb19844](https://github.com/user-attachments/assets/7c3a312d-c0dc-4c0a-b86f-0c4b00c0242e)


seq 10 | sed -n '4,6p'
## OUTPUT
![369745394-9a8791d4-f523-4540-9984-25850016f098](https://github.com/user-attachments/assets/2f689f47-a9ba-4a5d-aa0e-d24cea142110)


seq 10 | sed -n '2,4p'
## OUTPUT
![369745405-5dab593a-2ddd-4258-ae8a-c78d0d73bfa6](https://github.com/user-attachments/assets/5143f8bf-cf3d-4d27-affc-bd8da55cbcc6)

seq 3 | sed '2a hello'
## OUTPUT

![369745426-bd56fd0e-c4a1-494a-949b-ecdc495b7e3b](https://github.com/user-attachments/assets/ee9d021a-fde4-422f-a399-3f41548bc6df)

seq 2 | sed '2i hello' 
## OUTPUT
![369745426-bd56fd0e-c4a1-494a-949b-ecdc495b7e3b](https://github.com/user-attachments/assets/034c3e63-5de1-4e43-9a28-c4504400444a)


seq 10 | sed '2,9c hello'
## OUTPUT
![369745432-e08a0b76-43d7-4f08-8a18-0a87af358400](https://github.com/user-attachments/assets/c8fc52d1-9cd6-40eb-8ad0-5d5a2e6abdf5)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![369745441-a81727ab-4b40-4677-9209-3ccbb8fb0987](https://github.com/user-attachments/assets/a277bcd3-324d-4012-ac97-2ce6fcff9e0b)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![369745454-faf2e9f7-8ab4-4200-a3ac-318011b9682a](https://github.com/user-attachments/assets/20616b39-3da5-4ded-afe0-8d7575c204ec)

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
![369745526-b4392c86-82a0-4cb8-9578-3ec71c87151b](https://github.com/user-attachments/assets/dcba7d47-2c37-4b4f-874e-b24857367377)

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
![369745546-8d9e8b72-8230-4dca-9973-dbd71b6ec5dd](https://github.com/user-attachments/assets/22fc782c-8f2b-462b-b670-01dd29268854)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![369745587-9d5b0bd5-fa83-4c19-a7cf-3ff37666a8fd](https://github.com/user-attachments/assets/f7cba8de-d66e-49d2-96e0-94e5e2deb020)


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
![369745608-f9071865-280d-4ad6-a83b-e43d73f6e635](https://github.com/user-attachments/assets/72aa78e2-30f2-4bcb-973a-4ccb8ea3034c)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![369745613-caec1a3f-0fe9-4119-8b1a-5458c2862156](https://github.com/user-attachments/assets/9f11aff3-532e-4578-9402-4f458d8697b0)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![369745640-606f76c0-7793-418b-9408-33971f681475](https://github.com/user-attachments/assets/aa6fca59-d11a-4cf7-a3a6-a8f5d3ab52d6)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![369745659-3a294dd2-5af3-4a49-b55e-f99e57d4925a](https://github.com/user-attachments/assets/3c1e8d7d-51ae-4bd8-8fe5-15143a783731)


tar -xvf backup.tarr
## OUTPUT
![369745692-47f006bc-41b3-46a0-a9ce-bf57921c5f98](https://github.com/user-attachments/assets/cc0427ed-db47-44d6-ad75-54d252f17005)

gzip backup.tar

ls .gz 
 
gunzip backup.tar.gz
## OUTPUT
![369745696-bfa5f9b2-cf67-4758-b6ae-78b254628381](https://github.com/user-attachments/assets/353034ee-44db-4e65-84e3-e8095a7bf44b)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![369745892-9028a3e7-09d4-4826-9711-cc7c1358180e](https://github.com/user-attachments/assets/8a363720-f767-45f0-abc5-7f40e17689db)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/ebe47f51-c9fa-4037-a594-d19d9c811e7f)


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
![369745926-4630de64-b17f-403c-a136-d349e997b62d](https://github.com/user-attachments/assets/bd0a9a72-77dc-4182-bfb0-2e9a3ce6937f)

 
ls file1
## OUTPUT
![369745945-9c1c5a98-1c88-4f63-acda-a3941e2e8724](https://github.com/user-attachments/assets/42917246-00e8-498f-b04c-975e33ec7a17)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
![369745962-85477858-72f1-401f-a50b-6ee3a58bee38](https://github.com/user-attachments/assets/3bc802ad-92c5-48e2-aac8-6f6d3b3280d0)
 
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
![image](https://github.com/user-attachments/assets/de5e3456-715c-4644-9445-a969e2fcf325)

chmod 755 strcomp.sh
 ./strcomp.sh 
## OUTPUT
![369746040-11a32e51-8865-42bb-85a0-770b3789856a](https://github.com/user-attachments/assets/3111687e-96e3-42c9-9699-9c0f3c48b5e6)


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
![369746058-1174d68f-91b5-4131-979a-8dcf55945ea2](https://github.com/user-attachments/assets/b6f53358-5ee2-4119-8a6a-ef14643d710c)

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
![369746077-28783638-8466-4e7d-b88b-bb4fa72b67ca](https://github.com/user-attachments/assets/92c30023-ac0f-4974-afc0-322c719f05f3)


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
![369746153-49dc1ac1-a61f-4b37-b8fd-2d795b495523](https://github.com/user-attachments/assets/486e3813-368c-4091-b6ca-ca07f315e638)

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
![369747445-8c6fc40e-8579-4a5c-a59a-43808784b80a](https://github.com/user-attachments/assets/02f57832-bca9-4fd3-84ea-224bca7ef1c8)

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
![369747476-0a965529-d98c-423b-8edb-a7fb2d0fd29b](https://github.com/user-attachments/assets/2c737934-62a6-4d94-98ec-7b874fb72ffc)


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
![369747505-c5dd1c54-ddfa-49b8-9f06-abc66039b54a](https://github.com/user-attachments/assets/bb57c768-345a-4fe0-97f3-6f194c66d96b)

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
![369747548-a9a02c16-8f44-4912-8429-f06e02381141](https://github.com/user-attachments/assets/1ace6200-c3a1-47f6-8ef6-cf2f9f57652b)

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
![369747571-a581d9af-26d1-4fff-b0e0-0123c5b4b5b3](https://github.com/user-attachments/assets/978dddce-4d38-4876-bf6f-baad57e8a68a)


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
![369747592-dcf0fcbe-77a2-4702-8093-e9808058f67b](https://github.com/user-attachments/assets/2da4cc99-4aea-418e-a4c7-c4142ef6c674)

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
![369747586-8f8cee6b-d0bc-43a1-9c9b-03a7e1e2fd63](https://github.com/user-attachments/assets/a426631b-2353-4839-a30c-4ad2a8918b89)

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
![369747616-ef48bf6f-e809-4ee8-ba93-a2572017a2d8](https://github.com/user-attachments/assets/7d5a5a9f-6501-4569-98f6-3d4ab892cf34)

 
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
![369747633-360f1a97-4b28-4d2a-a6b0-5c31ed8067cf](https://github.com/user-attachments/assets/b1afccad-e645-4d0a-a107-1ef4e8d8031c)

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
 ![369747763-190f581b-b89f-40d8-866b-57c3cf509233](https://github.com/user-attachments/assets/ab9d5ac1-cd13-43dc-8c6f-386b037936ed)

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
![369747784-a69222a7-41d7-4afb-8481-066e7d0400d0](https://github.com/user-attachments/assets/c637561c-f5bd-4132-a83a-7a11ed399383)



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
 ![369747843-09c5e6a3-239d-4f40-80e4-26ad38e934da](https://github.com/user-attachments/assets/7def7a65-cb7d-42d7-9982-938d5cb4d33a)

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
 ![369747871-612ea892-4494-433d-a834-c187f95e1151](https://github.com/user-attachments/assets/41aec261-7171-4608-aef2-74cacd98b1c3)

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
 
 ![369747910-d62b0c59-a9f7-4e05-86cd-c25f51645177](https://github.com/user-attachments/assets/b6b0d3cf-b489-4597-8e27-0734639cab03)

 
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
 ![369747930-c92753e5-c24f-4736-b20a-8ed85bfdaeff](https://github.com/user-attachments/assets/0fcbab0c-68c8-40a4-9362-cfdf55846894)

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
![369747944-378f9ac8-e25b-47cb-af40-7c43e8bf4c18](https://github.com/user-attachments/assets/a543d273-673d-4c28-930c-8c83d3692de8)


# RESULT:
The Commands are executed successfully.
