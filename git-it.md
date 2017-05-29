Terminal (Bash) Commands 101
============================

## Create a new empty workspace
In Cloud9 create a new workspace using the HTML5 template. When it's finished initializing, you will see a new empty workspace. Locate your terminal at the bottom of your screen:

[![s1.png](https://s4.postimg.org/vj4j5npn1/image.png)](https://postimg.org/image/3vrtrk4g9/)

 We will be working in the terminal for the remainder of this workshop. Although you don't need to worry about this for now, note that this terminal uses a Bash shell and you will be learning Bash commands (this is standard for Mac and Linux).

## Check out the contents of your directory
```bash
ls
```
Use the command 'ls' to list all of the files in your current directory. You should see the README and hello-world.html files. Note that we are currently located in the root directory of your project workspace.

[![s2.png](https://s10.postimg.org/luu2jymjd/image.png)](https://postimg.org/image/5wlcttsb9/)

## Make a new directory
```bash
mkdir test
```
Use the command 'mkdir *directory_name*' to create a new directory. We'll just call it test. Once you execute the mkdir command, you can use ls again to make sure test is in your root directory.

[![s3.png](https://s30.postimg.org/kyvxrpf69/image.png)](https://postimg.org/image/jwlr95wct/)

## Change directory
```bash
cd test
```
Use the command 'cd *directory_name*' to move into the specified directory. You will notice that your terminal path will change from from /workspace to /workspace/test. Once you move into test, if you use ls again you will notice that nothing is listed. This is because your new directory is empty! We will fix this momentarily.

[![s4.png](https://s11.postimg.org/56h7mz8c3/image.png)](https://postimg.org/image/nyt2qk4q7/)

## Create a new file
```bash
touch index.html
```
Use the command 'touch *file_name*' to create a new file with the specified name and extension type. While touch is technically the command used to 'touch' a file and change the timestamp on its most recent access, it is also the easiest way to create a new file in bash as long as the given filename has not already been used. We will create a new html file called index (again, nothing to worry about for now but index is the standardized naming protocol for an html or js file that makes it the default file for imports and other reference related usages). You should see index.html appear under test in your workspace directory view in the lefthand side of Cloud9's interface. If you use ls, index.html should now be listed in the terminal as well.

[![s5.png](https://s10.postimg.org/v8uv1y6qx/image.png)](https://postimg.org/image/4b0y07m3p/)

## Edit your file and display its contents
```bash
cat index.html
```
Go ahead and add some text to your new html file. You can then use the command 'cat *file_name*' to display the contents of a specified file.

[![s6.png](https://s30.postimg.org/xqgq9li4h/image.png)](https://postimg.org/image/8x768xz3x/)

## Move back out of your directory
```bash
cd ..
```
Using '.' in bash specifies the current directory. If you do 'cd .' nothing will happen, because you're just changing to the current directory. However each subsequent '.' specifies the directory prior (assuming it exists). Using 'cd ..' will move you back one directory. Using 'cd ...' will move you back 2 directories. Using cd .... - you get the point. Note that '.' can be used to reference the current directory for many commands other than cd!

[![s7.png](https://s18.postimg.org/svhfdisrd/image.png)](https://postimg.org/image/bi74ynxg5/)

## Removing files/directory
```bash
rm index.html
rm -d test
```
Hope you didn't get too attached to your index.html file - now we're going to delete. To delete a file just use 'rm *file_name*'. cd into test, and call 'rm index.html'. Once you've deleted the file, cd back out of test (recall .. specifies the prior directory). Now we're going to delete the entire directory. If you try calling rm test you'll notice you get an error: 'rm: cannot remove ‘test’: Is a directory'. To remove a directory you need to include the -d flag. You can alternatively use the -r flag, which recursively deletes the entire file hierarchy rooted in the given file or directory parameter. BE CAREFUL USING COMMAND LINE DELETION! Especially with the -r flag. When you use the command line there is no going back. If you aren't careful you might accidentally delete all sorts of important files or entire directories. Make sure you pass it the right parameter and are rooted in the desired directory.

## Dealing with multiple files
```bash
touch f1.js f2.js f3.js f4.js
rm f*
```
If you want to create multiple files at once, you can use touch with multiple file names. This will create 4 new JavaScript (.js) files.  To delete all of them at once we can use rm f\*. The \* tells the command to be executed on files whose names contain an f followed by any number (this includes none) of any characters. If you are familiar with regular expressions, you will notice this uses the same syntax. Note that if you had any other files in your directory that started with the letter f they would also be deleted, so again be careful. The * can be used for many other commands to reference any number of files that might match.

## Moving and copying
```bash
mkdir humpety
mkdir dumpety
mv dumpety humpety
touch wall.js
cp wall.js humpety/dumpety
```
To move a file or directory just use the command 'mv *source* *dest*'. This moves the specified file/directory source to the desired destination path. In our example we will move the directory dumpety to be inside the directory humpety. We can also copy files or directories in a similar manner by using the command 'cp *source* *dest*'. In our example we create a file wall.js and copy it into dumpety (which remember has been moved to be inside humpety). Note that if you want to move a directory instead of a file you will have to use the -r flag, similar to what we saw with the rm command.
