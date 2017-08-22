# Linux tips for Pi NOOBS
These are general linux tips that may make your Raspberry Pi experience more enjoyable, particularly if you use the terminal (or SSH) a lot.

#### Install midnight commander - sudo apt-get install mc.
This will make traversing the filesystem much easier, and streamline a lot of workflow

#### Use nohup to run commands after you close an SSH session.
If you access your Pi by SSH, and want to start up a process that takes a long time to run (like a large download or update) but you still want to be able to close the SSH session, preceed it with nohup, eg:
`nohup sudo apt-get upgrade`
Now you can close your shell session without aborting the process

#### Pause and Restore commands
Pause an application with `Ctrl+z` and restore by executing `fg`.
How many times have you been editing a file with nano and had to go refer to some file, directory or run some command. The naive approach is to save+close nano, execute the command, and reopen nano.
Instead, try pausing with `Ctrl+Z`. You'll see that nano has been added to a stack of paused programs. Continue with your business and then recall nano to the _foreground_ by executing `fg`
