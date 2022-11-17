# Linux Commands

## ${\color{orange}WILDCARDS}$

>| Operator | Description | Example  |
>| :--------- | :--------- | :--------- |
>|*	|Matches n character or we can say all character|
>|?	 |Matches only one character|
>|{}	|Used to give the range to pefrom the task n t|
>|[]	|Used to find any later present inside bracket |example-> ls -la *[cd]*|
>|/usr/bin or /usr/sbin	|All the system commands are present in this folder|
>|chown	|Used to change the user of file/dir  |
>|Chgrp 	|Used to change the group of file/dir|
>|chmod	|Used to change the permission of file/dir|
>|Groupadd	|Used to add group|
>|Groupmod	|Used to update created group|
>|Ueradd /adduser	|Used to add user|
>|usermod	|Used to update the user|

<br>

***

<br>

## ${\color{orange}LS}$
Used to find check the content of director
    
>| Option     | Description | 
>| :--------- | :---------  |
>|-l	         |Give the list form of content |
>|-n	         |Give the info about GID and UID of directory|
>|-a	         |Used to see all hidden file too|
>|-A	         |Used to see all the hidden file without . And ..|
>|-lt	     |Used to sort files according to time|
>|-s	         |Show file size|
>|-h	         |show file size in human readable form |
>|—author	 |Print the name of the user|
>|-d          |	Print only list of directory|
>|1	         |Print the list in vertical lin|

<br>

***

<br>

## ${\color{orange}MAN}$

    1. Used to get the manual of the command 
>| Options  | Description         |
>|---       |---                  |
>|-f	       |Used to give the short description of the command  |
>|-w	       |Used to get the location of the command|

<br>

***

<br>

## ${\color{orange}MKDIR}$

    1. Used to create the directory in the system 
	2. mkdir path/folder_name
>|Options    | Description  |
>|---        |----          |    
>|-p	        |Used to create the parent also if not presented|
>|Relative path 	|Starting from current directory|
>|Absolute path	|Starting from home directory |

<br>

***

<br>

## ${\color{orange}Home}$
    1. Moving directly to the home directory
   
>|Options    | Description  |
>|---        |----          |    
>|Cd $	|Redirection toward home directory|
>|Cd ~	|Redirection toward home directory|

<br>

***

<br>

## ${\color{orange}RMDIR ~/ ~RM}$
    1. Removing Directory / File from the system
    2. rmdir folder_path
    3. rm path/folder of file
   
>|options    | Description  |
>|---        |----          |    
>|-p	|Removing the parent with the child|
>|-rf	|Removing the directory with the content as well|

<br>

***

<br>

## ${\color{orange}TOUCH}$
    1. Used to create the file in the system
    2.  Touch path/filen_name

<br>

***

<br>

## ${\color{orange}PIPE}$
    1. Used to write multiple command in single line
    2. Output of one command is passed to next command
    3.  Command | command | command

<br>

***

<br>

## ${\color{orange}WC}$
    1. Used to count the details of the file such as number of line, word count and character of the file 
    2.  WC filename
    3. To get the particular details of the file used
>|options    | Description  |
>|---        |----          |    
>| -L	    |Number of line used|
>|-w	        |Total words|
>|-m	        |Total byte count|
>|-c	        |Total character count |

<br>

***

<br>

## ${\color{orange}Seperators}$
>	Used to write in file with overwrite functionality
>>	Used to write in file with append functionality 

<br>

***

<br>

## ${\color{orange}AWK }$
    1. Used to print the word for the given number
    2. Cat file | awk ‘{print $1, $2,$NF}’ -> it will print the first word which comes from cat file command  NF -> last word
    3. It is also used to find the deta in file 
        1. Awk ‘/pattern/ {print}’ filename
    4. Finding data less or more than requirement
        1. Awk ‘length($X) >/< X’ filename
    5. Applying condition
        1. Awk ‘{if(condiction) print}’ filename
            1. Eg -> awk ‘’{if($0 == a ) print}’ new.txt

<br>

***

<br>

## ${\color{orange}Reading files}$
>|||
>|---|---| 
>|View file_name|	Reading file
>|More filename	|Next line on enter and q for exit
>|Less filename|	Next line on enter and q for exit and we can use arrows to go back and forth
>|Head -nX	|Used to read top Lines of the file (by default it is set to 10 lines)                             [X-> number]
>|Tail -nX	|Used to read last Lines of the file (by default it is set to 10 lines) [X-> number]

<br>

***

<br>

## ${\color{orange}CP}$
    1. Used to copy the file and directory from one location to other 
    2. cp source destination
    3. While copy we can change the file/folder name also

>|options    | Description  |
>|---        |----          |  
>|-r	|Used when our folder is not empty and we have to transfer file in that folder also [recursively]|

<br>

***

<br>

## ${\color{orange}MV}$
    1. Used to copy file/folder from one location to other
    2. Mv source destination
    3. While move we can change the file/folder name also

<br>

***

<br>

## ${\color{orange}DIFF}$
    1. Used to find the difference between files
    2. Diff file1 file2

<br>

***

<br>

## ${\color{orange}CUT}$
    1. Used to cut the file with separators [same as split in python]
    2. Cut -d[‘separator symbol’] -fX[number of the word we need] filename
    3. To get the particular word in a file cut -cX,X-X file_name

<br>

***

<br>

## ${\color{orange}COMM}$
    1. Used to find the common from the file 
    2. comm file1 file2

<br>

***

<br>

## ${\color{orange}SED}$
    1. Used to set the text on current text but did not affect the current text [same work as replace in python]
    2. Echo ‘hello’ | sed ’s/hello/vaibhav/g’. —> output vaibhav
    3. g stands for global 
    4. -I issued to update the changes in the file 
>    5. To delete the line matching the string we used 
>>       1. Sed ‘/name/d’ file name
>    6. Deleting X line
>>       1. sed ‘1d’ fike_name
>>       2. sed ‘1,2d’ file_name
>>         1. 1 -> remove line 1
>>         2. 1,2 remove line 1 and 2
>    7. Removing empty line from file
>>        1. Sed ‘/^$/d’ file_name
>    8. Adding space after every line 
>>        1. Sed G filename
>    9. Adding changes except one line 
>>        1. Sed ‘X!s///’ file_name

<br>

***

<br>

## ${\color{orange}TEE}$
    1. Tee is used to write in file and we dont have to pass any separators as we have to do in cat
    2. tee file name

<br>

***

<br>

## ${\color{orange}TR}$
    1. Used to translate the text [like we have to change one character to another we use tr]
    2. Echo ‘’Hello” | tr  ‘el’ ‘EL’

<br>

***

<br>

## ${\color{orange}FIND}$
    1. Used to find the file in system 
    2. Find folder_name  type [like -name] filename

<br>

***

<br>

## ${\color{orange}LOCATE}$
    1. It is used to locate the file in database instead of file system

>|LOACTE    | FIND  |
>|---        |----          |  
>|It is used to find the file in datbase	|It is used to find the file in file system|
>|Fast as compared to find	|slow|
>|We don’t have to give any location just type locate filename	|It needs all the folder path type to find it|
>|To locate the file database should be updated 	|There is no requirement to update the datbase |

<br>

***

<br>

## ${\color{orange}UID}$
    UID -> Unique user id
>|TYPE    | Description  |
>|---        |----          |  
>|0	|Reserved for root |
>|1-99	|Reserved for predefined account|
>|100-999|	Resered for system admin|
>|1000-	|Open for the uers|

<br>

***

<br>

## ${\color{orange}GID}$
    GID -> Group identifier
>|options    | Description  |
>|---        |----          |  
>|0	|Reserved for root|
>|1-99	|Reserved for applications|
>|100-	|Open for everybody|

<br>

***

<br>

## ${\color{orange}BASIC~FILE~STRUCTURE}$
    1. passwd -> 
        1. Store the info about the users, group, shell, password 
        2. But password is not stored here 
        3. Location -> /etc/passwd
        4. Username : passwd : uid : Gid : description : homedir : shell
    2. Shell file ->
        1. Used to store the info about the shell present in the system
        2. Location -> /etc/shells
    3. shadow ->
        1. This file store the info about the password of user
        2. Location -> /etc/shadow
        3. Username : hasedpass : last_pass_changed_days [from 1 jan 1970] : min age of pass : max_age_pass : inactive days
>|options    | Description  |
>|---        |----          |  
>|*	|No passowrd|
>|Hashed	|Password is hidden with logs|
>|!	|Passowrd is never set|
	4. Group File->
		1. Used to store the group info and the user assigned to the group
		2. Location -> /etc/group
		3. gname : pass : id : user_belong to group
	5. Group password file
		1. Used to some the info about group password [encrypted]
		2. Location -> /etc/gshadow

<br>

***

<br>

## ${\color{orange}WHICH~/~WHATIS}$
    1. Which is used to find the location of the command
    2. What’s used to return the shot description of the command

<br>

***

<br>

## ${\color{orange}ADDING~~USER}$
    1. There are two methods from which we can add user -> 
        1. Useradd
        2. adduser
    2. Adduser is the interactive way to add user and in background it uses useradd to create user
    3. Useradd->
>|options    | Description  |
>|---        |----          |  
>|-d	|Used to manipulate the used home directory|
>|-p	|Used to set the password|
>|-c	|Used to add description |
>|-s	|Used to add shell for user|
>|-m	|Used to create home directory|
        # Basic command -> Usedadd -m new_user

<br>

***

<br>

## ${\color{orange}PASSWD}$
    1. Used to add the new password for the user
    2. Passwd  username
    3. If we don’t pass the user name then it will update the current user password

<br>

***

<br>

## ${\color{orange}USERMOD}$
    1. Used to manipulate the setteing to current user 
    2. Usermod username
>| Options    | Description  |
>|---        |----          |
>|-c	|Adding comment
>|-d	|Manipulation home directory
>|-g	|updating primary group
>|-G	|Updating secondary group 
>|-s	|Updating shell
>|-p	|Updating password
>|-u	|Updating userid
>|-a	|Used to append user to other group  without removing it From current group         

<br>

***

<br>

## ${\color{orange}FILE}$
    1. Used to give the type of the file 
    2. Files are classified into different types

>|  Types    | MEANING  |  DESCRIPTION   |
>|---        |----          | --- |
>|-	|Regular file	|
>|d	|Directory	|
>|b	|Block file	|
>|l	|Symbolic file 	|Files or directory which are pointing to other file or directory|
>|-	|Hardlink file	|
>|s	|Socket file 	|The files which create the communication between tow process
>|p	|Pipefile	

<br>

***

<br>

## ${\color{orange}VIM}$
    1. It is the file editor tool used to update and create file 
    2. VIM run on three more insert [ i ],  command[ : ], execute [default] mode

<br>

***

<br>

## ${\color{orange}META~~DATA}$
    1. INODE contains the meta data of the file except its name and data
    2. To see the anode of the data we write 
        1. Ls -i
    3. To check the stats of the file we use
        1. Stat file/dir

<br>

***

<br>

## ${\color{orange}Links ~~[hard/soft]}$ 
    1. Links works as connection between same file substituted in different location for easy access [name can be difference but inode will be same]
    2. Types of line —> soft link, hardlink
        1.  HardLink 
            1. It is excact copy of main file which take same space as original file
            2. If main file will be deleted there will be second file sorted in the system without any data loss
            3. Command -> ln file1 new_file2
        2. SoftLink
            1. It is excact copy of main file but the size will be less than original file
            2. If main file will be deleted then the data present in softlink will also be vanish
            3. Command -> ln -s file new_file

<br>

***

<br>

## ${\color{orange}REDIRECTIONS}$
    1. Saving the input, output and errors in file we use re directions
>|Type	|Description	|Process	|Example
>|---|---|---|---|
>Input redirection| 	Keyboard input	|Cat > or >> filename 	|Cat > file.txt
>Output|	Output of other command	|Command > or >> fname	|Echo ‘’Hello” > file.txt
>Error |	After running something and we get error so to store the error we use|	Command 2> or 2>> fname|	Sum 2> file.txt [as sum is not a command it will store error]
>output and error|	If command give output as well but gives error so we need to store the error also so we use this reduction|	Command &> or &>> fname	

<br>

***

<br>

## ${\color{orange}SU}$
    1. It is used to login to the user shell
    2. su user_name

<br>

***

<br>

## ${\color{orange}CHAGE}$
    1. It is the command used to change the life span of the password for user 
    2. IT is managed by the admin
    3. chage -options user_name [-m Min age, -M max age]

<br>

***

<br>

## ${\color{orange}GROUPADD}$
    1. Used to add group to the system
    2. groupadd -options new_name


>| Options    | Description  |
>|---        |----          |
>|-g	|Used to give the GID to gropu|
>|-o	|Used to create group with same kid|
>|-p	|Used to set the password for the group|

<br>

***

<br>

## ${\color{orange}USERDEL}$
    1. Used to delete user from the system 
    2. userdel -opetions user_name
>| Options    | Description  |
>|---        |----          |
>|-f	|Forcefully remove all the files|
>|-r	|Remove home directory|

<br>

***

<br>

## ${\color{orange}SUDO}$ 
    1. Superuser do/ Substitute user do
    2. Most important part in which we provide user to run some specific command to run on root
    3. We have to set permission which user can run which cammand on root level from their logon
    4. Sudo given_permission
    5. To give the permission we have to of to /etc/sudoers.d/ [we don’t directly update doers as to can issue can’t affect out root file]

<br>

***

<br>

## ${\color{orange}PERMISSIONS~~IN~~LINUX}$
    1. There are three type of permission in linux
>|Permissions 	|Symbolic text	|Numeric method|
>|---|---|---|
>|READ |	r	|4
>|WRITE	|w|	2
>|EXECUTE	|x	|1
    2. General Formate of permission -> user group others                                                           [rwx   rwx    rwx ]

<br>

***

<br>

## ${\color{orange}CHOWN}$
    1. Used to change the owner of the file or directory
    2. Chown user_name file/dir
   
<br>

***

<br>

## ${\color{orange}CHGRP}$
    1. Used to change the group of the file or directory
    2. Chgrp grp_name file/dir 

<br>

***

<br>

## ${\color{orange}CHOWN}$
    1. To change user and group name in same command 
    2. Chown username:grpname file/dir

<br>

***

<br>

## ${\color{orange}CHMOD}$
    1. Used to change the permission of the directory
    2. chmod ugo [4+2+1,4+2+1,4+2+1] file/dir
    3. Chmod [ugo] +rwx or -rwx file/dir [example -> chmod u+rw g+rw o-r file (ug -> write o-> no read)

<br>

***

<br>

## ${\color{orange}GROUPDEL}$
    1. Used to delete the group from the system
    2. Groupdel group_nam

<br>

***

<br>

## ${\color{orange}File structure}$
     File Used in linux and their meaning 
  <IMG style='width:100%; height:400px' SRC='./file-type.JPEG'/>

<br>

***

<br>

## ${\color{orange}ACL}$
    1. Its is the permission giving mechanism for file system
    2. Senerio -> If permission is given to a group and with that we want to give a new user permission to that file but we don’t. Want to add that user in group so without adding to that group we give them permission using ACL
    3. Setting permission 
        1. Setfacl -m u:username:permission file_path 
            1. -m stands for modify
            2. -x stands for remove persmissom ,permission part will be removed   rest whole command will be same 
        2. Getfacl


## ${\color{orange}SORT}$
    1. Used to sort the data 
    2. Sort file_name/command
   
|Options | Description |
| ---    |  ---        |
|-kX     | Sorting based on character number|
|-r      | Sort in reverse order|

<br>

***

<br>

## ${\color{orange}UNIQ}$
    1. Help to find the unique in the file 
    2. To apply uniq, the best practice is to sort the dat first and then apply uniq
|Options	|Description|
|---	|---|
|-c	|Show the count how many times the word occurress in file
|-d	|Shows only repeated words

<br>

***

<br>

## ${\color{orange}ZIP}$
    1. Used to compresse a file 
    2. tar, gzip, bzip
    3. tar cvf filename.tar folder/file
    4. c -> create
    5. v -> verbose
    6. f -> fourcefuly


<br>

***

<br>

## ${\color{orange}Truncate}$
    1. Used to add or delete the file size 
    2. Truncate -option size filename 
|Options|	Description|
|---|---|
|-s	|Used to add or remove the byte assign to the file  |
    3. It will not compress the file so be careful while using the option

<br>

***

<br>

## ${\color{orange}Split}$
    1. Used to split the file according to our need
    2. Split -l line_numbers file_name
    3. It will slip the file based on one number and create a own name for each file when every if split the file in line numbers

<br>

***

<br>

## ${\color{orange}User mentoring }$
>|command|description|
>|---|---|
>|who|tells how many people are login to system and >terminal numbers|
>|last|tells who login into system from start|
>|w|same as who but tells move info like cup usage and all|
>|pinky|tells who in currently login to the system|
>|id|tell the uid, gid of user|

<br>

***

<br>

## ${\color{orange}Talking~~to~~user}$
>|Command|Description|
>|---|---|
>|user|tells the name of the active uses|
>|wall|sending msg to all the users |
>|which usern|sending message to particular active user|