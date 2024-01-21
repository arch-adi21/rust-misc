## Discussing error in brief
> This error arises in two cases :-
<br>
**1.** If you used the methode _cargo build_ -> _cargo run_ to create your main.rs and then created your rust code , you are facing this issue because u haven't updated the dependancies yet. There is a part in your **Cargo.toml** file , which is responsible to install all the extra dependancies for your code.
### how to fix this ?
-> navigate to the base folder of your project. The name will be same what gave in ```cargo new folder_name``` as folder name. 
