# linux-notes

Create a folder with a subfolder. 
````
mkdir -p workspace/folder/subfolder
````
This creates both folder and the subfolder inside it. 

ls -lh 
See file contents and permissions
rmdir - remove directories (removes empty folder only)

cp/mv/  
 either be used to name the duplicate, or specify a filepath for the duplicate.
mv is also used to rename files. 


mv *.txt 
Moves all files ending with .txt to filepath. By itself, asterisk indicates all files in the folder. 

mv folder/subfolder/* . 
Moves all the files in subfolder to the current directory (.). 

rm  
Deletes files. 

rm file?.txt 
? - wild card character- would delete file1, file2, file3 etc.

rm -r 
Recursively deletes files inside 'file' 

find  -name "poe*" 
Looks for files inside file with names that start with poe 

su root 
Switch to root (admin) user 

./
How to run an executable from the command line (executable- can run on its own, without being loaded by another program). 

File Permissions 

rwx - read, write, execute 

In order of User/owner, Group, Others
rwx-rwx-rwx
owner-group-others

chmod
Used to change the file permission by changing the file mode bits 

Ways to represent permissions
- Octal notation
- Symbolic notation 

Octal Notation- 3 numbers like 777
Each digit represents the privilege breakdown as a sum: 
Read (4) Write (2) Execute (1) 
rwx = 7 
r-x = 5 
r-- = 4


Symbolic 
User (u), Group (g), Others (o), All classes (ugo) (a) 
+: adds permission; -: removes permission =: adds permission but removes others 

Always chmod <code> filename 
Where code is symbolic or octal notation 


Pipe character (|) 
Used to connect commands together at the command line. 
ex: 
echo "Hello" | wc 
Output of wc, word count, is displayed, not the Hello 
wc output: (lines) (words) (characters) 

cat- Concatenate or print files, used to see contants of a file, or take the contents and pipe them 

head, tail can be used to see parts of file, with -n as number of lines 

head -n 5 poems.txt 

cat poems.txt | cat -n | tail -n 5 
Original file content is piped into cat -n command which numbers it, and then tail displays the last 5 lines. 

less  
Lets you view a file with a bit of an interface (can use f/b, enter/spacebar) 

grep- search files for text matching a regular expression, prints them out 

grep -n "the" poems.txt  
Shows every line that contains "the", -n adds numbers (case sensitive) 
-i arg makes it case-insensitive 

awk 
Extracts particular data from a file

awk '{print $2}' simple_data.txt 
Single quotes contain the awk program 

sed - stream editor
Used for changing data

sed s/Orange/Red/ data.txt 
Substitutes a string with another string in a file. 


sort- use K to 

