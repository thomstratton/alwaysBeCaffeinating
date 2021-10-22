# Always Be Caffeinating - prevent mac from going to sleep.

This will set up a launchd controlled daemon to start up on boot which prevents the MacOS computer from going to sleep by utilizing the builtin caffeinate command.  (May be needed for some situations).  Make sure this is really needed before you use it... don't waste energy for no reason!

## installation

Download com.stuffwecode.abc.plist, open terminal, and change to the folder where you downloaded the plist.  e.g.

```console
cd ~/Downloads/alwaysBeCaffeinating
sudo cp com.stuffwecode.abc.plist /Library/LaunchDaemons
sudo launchctl load /Library/LaunchDaemons/com.stuffwecode.abc.plist
```

## verification

- you should see caffeinate listed are running with the command below.

```console
ps -ef | grep caffeinate
```

## configuration

- you can use any command line options supported by caffeinate in place of the default ( -dimsu ) by editing the ProgramArguments in the plist.  First argument needs to remain the caffeinate command itself as listed.

## manual start / stop

```console
sudo launchctl load /Library/LaunchDaemons/com.stuffwecode.abc.plist 
sudo launchctl unload /Library/LaunchDaemons/com.stuffwecode.abc.plist
```
