# FIle_system_implementation_using_link_list_data_structure_in_C_language
It is an imaginary file system. User will be able to create, delete or edit a file or folder. Note that this operations will not actually create a folder or a file in your real file system. You will just need to implement a tree structure to pretend like you are performing user requests. Your linked list and tree structure might look like as below.

Single boxes are files , singel arrows are pointers to next double boxes are folders and souble arrows are pointers to the next child item in the folder.
There is no pointer to a parent in this system or design, but we modify it according to the our requirements. we must implement this system or design using linked list, pointers, structure and memory allocation [Dynamic] in C Language.

Our file structure would possibly have.

char* name;
int numberOfItems;
int size;
int date;
struct Node* next;
struct Node* child;

When we run our program, we should see an empty command line waiting for our command. Let’s assume your file-folder structure is empty at beginning (In your actual submission, you will start with a sample file-folder structure.). Then, suppose we enter a creating new directory command:

> mkdir sem1

Then you should create a folder structure variable with necessary attributes. Then, if we call “ls”, you should list the files and folders inside the current folder like following:

> mkdir sem1
> ls
0items 21 Jun 21:55 sem1
>

Let’s create a file and list again:

> mkdir sem1
> ls
0items 21 Sep 21:55 sem1
> touch data_structures.txt
> ls
0items 21 Jun 22:10 sem1
0B     21 Jun 22:15 data_structures.txt
>

Enter some text to the file and do some more operations:

> mkdir sem1
> ls
0items 21 Jun 21:55 sem1
> touch data_structures.txt
> ls

> cd sem1
> touch dbms.txt
> ls
46B    21 Jun 22:01 data_structures.txt
0B     21 Jun 22:04 dbms.txt
> pwd
/courses
> cdup
> ls 
1items 21 Jun 21:55 courses
> lsrecursive
1items 21 Jun 21:55 courses
|_46B    21 Jun 22:01 data_structures.txt
|_0B     21 Jun 22:04 dbms.txt




we will implement the commands to handle file system :

Command 	                                      
ls            ==>  Lists the content of the current directory. 
mkdir         ==>  Creates a directory
rm 	          ==>  Removes a file or a folder with all of its content.
cd 	          ==>  Change directory
cdup 	        ==>  Change current directory to parent directory
edit 	        ==>  Overwrite content of a text file with the entered text
touch 	      ==>  To make file.

Note :
Install 64bit Ubuntu on VirtualBox. Use Eclipse as your IDE. Codes written in Windows might not work on Ubuntu (different system calls).
