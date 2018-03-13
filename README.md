# Set up Bash(Ubuntu) in Cmder :fire: :fireworks:

If you haven't installed bash on your **Windows 10**, then :point_right: [Follow this tutorial](http://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)

If you don't have **Cmder**, get it from [here](http://cmder.net).

Launch **Cmder**, and press `Win + Alt + T` to open up the settings dialog for Tasks.

Alternatively you can open up the hamburger menu on the bottom right of the window and navigate to:
`Settings -> Startup -> Tasks`.

### Step 1

You create a new Task by clicking on the ‘+‘ Button at the bottom and enter the details.

### Step 2

The first input field of the dialog is the task name.
I named it `Ubuntu::bash` but the naming is completely up to you.
You can use double c
olons for grouping, so this would be the `Bash` task in the `Ubuntu` group. Cmder already comes with a `Bash` group containing entries for Bash on mintty (using Cygwin) and another one based on `git-for-windows`. To distinguish between the other Bashes and the ‘real’ Ubuntu thing, I simply chose to also opt into this naming scheme.

### Step 3

In the `Task parameters` input you can configure an icon
```
/icon "%USERPROFILE%\AppData\Local\lxss\bash.ico"
```

> _Sometimes the icon is not available in that directory. Try to look into this directory: `C:\Program Files\WindowsApps\CanonicalGroupLimited.UbuntuonWindows_VERSION\images` there. the `CanonicalGroupLimited.UbuntuonWindows_VERSION` would be different as per the installations. Or download the icon from internet_


### Step 4
In the `Commands` input field, you enter the command that this task should start. This is the actual call to Bash:

```
%windir%\system32\bash.exe ~ -cur_console:p
```
Now you have **bash** in your **Cmder** console :fire:


# Set up Zsh in Cmder

Create a new task `Ubuntu::zsh`, but again the naming is up to you.

Same task parameters as for the Bash task and just added `-c zsh` to the command entry.

This will cause `Bash.exe` to start `Zsh` automatically.

The full line is:
```
%windir%\system32\bash.exe ~ -c zsh -cur_console:p
```

Now just create new console by clicking on Green + button and select console as `{Ubuntu::zsh}` or `{Ubuntu::bash}` from first combobox and click on start enjoy :fire:

Now you can install [oh-my-ZSH](http://ohmyz.sh/) in your zsh for cool themes :sunglasses:

