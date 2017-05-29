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
Use the command 'touch *file_name*' to create a new file with the specified name and extension type. While touch is technically the command used to 'touch' a file and change the timestamp on its most recent access, it is also the easiest way to create a new file in bash as long as the given filename has not already been used. We will create a new html file called index (again, nothing to worry about for now but index is the standardized naming protocol for an html or js file that makes it the default file for imports and other reference related usages). You should see index.html appear under test in your workspace directory view in the lefthand side of Cloud9's interface. If you use ls index.html should now be listed in the terminal as well.

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
