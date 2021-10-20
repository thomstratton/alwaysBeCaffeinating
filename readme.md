# Always Be Caffeinating - prevent mac from going to sleep.

This will set up a launchd controlled daemon to start up on boot which prevents the MacOS computer from going to sleepby utilizing the builtin caffeinate command.  (May be needed for server workloads)

## installation

Download com.stuffwecode.abc.plist, open terminal, and change to the folder where you downloaded the plist.  e.g.

~~~console
cd ~/Downloads/alwaysBeCaffeinating
sudo cp com.stuffwecode.abc.plist /Library/LaunchDaemons
sudo launchctl load /Library/LaunchDaemons/com.stuffwecode.abc.plist
~~~
