
## Discussing error in brief
<br>
This error arises in two cases :-
<br>

### 1. Forgot to update dependency information in Cargo.toml
If you used the method _cargo build_ -> _cargo run_ to create your main.rs and then created your rust code , you are facing this issue because u haven't updated the dependencies yet. There is a part in your **Cargo.toml** file , which is responsible to install all the extra dependencies for your code.
#### how to fix this ?
-> navigate to the base folder of your project. The name will be same what gave in ```cargo new folder_name``` as _folder_name_. In my case I created the folder in Desktop/ directory with a name _guide_ for my convenience , so my navigation will look like following :-
```
$ cd Desktop/
$ cd guide
```
-> Now open ```Cargo.toml``` file in any code editor you wish. I prefer to use Neovim for editing so the command goes like ```nvim Cargo.toml``` . 
>If you use vscode , go to the directory and use ```code .``` to open the directory in vscode and then open the the file through the code editor. This will look like 
>```
>$ cd Desktop/
>$ cd guide
>$ code .
>```	
-> Now find the ```[dependencies]``` section in the _.toml_ file. Like one present in the image below
![image](https://github.com/arch-adi21/rust-misc/assets/155255348/89fc4063-9f44-489e-89db-7c87edea0b8c)
-> You can now add your dependencies in the format ```dependency_name = "version"``` . 
-> Now type the following commands one by one to _build_ and _run_ your code ```main.rs```.
```
$ cargo build
$ cargo run
```
-> **Now this will solve your error.**

### 2. Not using  ```cargo new folder_name``` to create your project directory
There are cases were people just create a folder and manually create ```main.rs``` file and they don't know how to add the dependencies in the file. Here instead of using ```cargo build``` and ```cargo run``` we use the following code
```
$ rustc main.rs
$ ./main.rs
```
### How to fix this ?
-> just copy the code of main.rs , build a new directory with ```cargo new``` , navigate to /src directory , open the main.rs file , paste the code in this new main.rs and start following the method in point _'1. Forgot to update dependency information in Cargo.toml'_ . The steps to navigate to this new ```main.rs``` file is listed down here :
```
$ cd Desktop/
$ cargo new folder_name
$ cd
$ cd Desktop/folder_name/src
$ nvim main.rs
```

> You can also do this in vscode by the process mentioned in the 1st bullet point .

Thank you for reading.
