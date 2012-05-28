homeshick
=========
<div style="float: right"><img src="http://i.imgur.com/3zAK9.jpg"></div>
homs**h**ick is a dependency-free alternative to [homesick](https://github.com/technicalpickles/homesick) (except git+bash)

# homeshick vs. homesick #
The goal is to mimick homesick in functionality.
_Functionality_ does however not include:
* **reliability**. technicalpickles has created a ton of tests for his tool, I'm not going to do that.
* **prompting**. When conflicts arise (symlink, track etc.) homesick prompts you nicely about what you want to do
  and gives you a wide range of options. It's too much of a hassle to do this in bash.
  Instead _homeshick_ simply compiles a list of stuff you have to do manually (except with symlink file overwrites).
* **gem** With _gem_ you can easily install and update homesick. That's a bit harder with a simple shell script.
* **runtime options**. For now, there are no runtime options because I focused on the core features,
  they may come in a future version.
* **tersity**. homesick hides a lot of git output. homeshick doesn't.
If anyone were to send a pull request fixing one/some of the above, I would be very grateful.

One advantage homshick has over homesick is the ability to install it easily without root privileges.
To install a gem, no root privileges make the job a lot harder (in my experience).
With homshick you simply run the three commands listed below and you are done!

# Installation #
Get the latest version of the script
```
    curl -so .homeshick https://raw.github.com/andsens/homeshick/master/homeshick
```
make the script executable and alias it in your .bashrc or .zshrc
```
    chmod +x homeshick
    printf "\nalias homesick=\"$HOME/homeshick\"" >> .bashrc
```
