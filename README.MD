# Linux tips
These are general linux tips that may make your Linux (and Raspberry Pi) experience more enjoyable, particularly if you use the terminal (or SSH) a lot.
If you have any sweet tips you think belong on this list, submit a pull-request

### Command history
Execute `history` to see your session's command history, and recall a command with `!<index>`
eg. recall command number: 321 with `!321`

**Execute the previous command, but with sudo**: `sudo !!`

For when you attempt to execute a command, it fails because you need permissions. Save up-arrowing to recall the command and then keying to the start of the line to add `sudo`


### Use nohup to run commands after you close an SSH session.
If you access your Pi by SSH, and want to start up a process that takes a long time to run (like a large download or update) but you still want to be able to close the SSH session, preceed it with nohup, eg:
`nohup sudo apt-get upgrade`
Now you can close your shell session without aborting the process

### Pause and Restore commands
Pause an application with `Ctrl+z` and restore by executing `fg`.
How many times have you been editing a file with nano and had to go refer to some file, directory or run some command. The naive approach is to save+close nano, execute the command, and reopen nano.
Instead, try pausing with `Ctrl+Z`. You'll see that nano has been added to a stack of paused programs. Continue with your business and then recall nano to the _foreground_ by executing `fg`.
Execute `jobs` to see the list of tasks sitting in the background.

### File Managers
**Ranger**: `sudo apt-get install ranger`
Traverse the filesystem very quickly
Split-window managers like _midnight commander_ also exist, but I find ranger faster and easier to manage.
