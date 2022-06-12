# 1. About included Termux versions

This directory contains a modified version of android terminal emulator and a Termux compatible version of TermVim.

Termux is a terminal emulator distributed on Google Play with various unix tools. Termux is not for Vim only, but for realizing a general Linux environment on Android. There is a set of command line tools such as 'clang', 'apt' and 'ssh' that can be installed by CLI.

**Termux Links:**
- https://play.google.com/store/apps/details?id=com.termux
- https://github.com/termux
- https://sites.google.com/site/fudist/Home/qfixhowm/other-service/howm-android#TOC-Termux

**!!! Important !!!**
This Termux version is a compatible app, so you should be able install it at the same time as the original Termux. If it won't, uninstall the original version before installing.

_See below for parts other than Termux._

 ## TermVim
 - https://sites.google.com/site/fudist/Home/qfixhowm/other-service/howm-android/term-vim

 --termux-vim-release.apk (Termux version)

 ## Modified version of Android Terminal Emulator
 - https://sites.google.com/site/fudist/Home/qfixhowm/other-service/howm-android/android-terminal-emulator-mod

 --term-termux-release.apk (Termux version)

 # 2. How to use the Termux command line

This modified version of Android Terminal Emulator (Termux version) is based on Termux. At first startup the code will be installed automatically. TermVim (Termux version) does not install Termux automatically, so is it `: shell`? You need to go into the shell with `Ctrl + z` and run` termux.install`.

After Termux is installed, Termux bash starts with `termux.bash` and Termux frame will be usable.

 When executing for the first time, execute the following command to update.

     $ apt update
     $ apt upgrade

 After that, it works like Termux. However, if you want to use the ALT key with Emacs etc., you can have select "Send ESC with ALT key" in "Settings". If it is not effective, it may not work.

 Note that Termux's Vim cannot handle Japanese other than UTF.
 If you want to call the TermVim version of Vim from Termux, run `$ APPFILES / bin / vim`
 please.

 After that, execute termux.bash as needed, or select "Initial command" or "Shell" in "Settings". Please set "Settings" appropriately and start Termux automatically.

However, if you want to set $ TMPDIR, put an appropriate directory under $ HOME or $ APPBASE ($ APPFILES). It's recommended that you create and set it. Other than that, if you don't set $ TMPDIR, some commands may not work. (In termux.bash etc., it is set to `$ APPFILES / usr / tmp`)

 # 3. Use Termux commands from Android standard shell

 Commands installed with Termux are basically supposed to work with Termux bash. There are commands that do not work with Termux, so you usually use a standard shell and need to, if necessary, use the method of invoking a command on Termux via a shell script.

 ## Call the Termux command from a standard shell

 For example, if you want to use Termux git from Android standard shell, it will be as follows.

 Launch Termux bash and install git.
     $ termux.bash
     $ apt install git
     $ exit

 Then rename `$ APPFILES / bin / termux.cmd.sh` to` git` and run it.

     $ cp $ APPILES / bin / termux.cmd.sh $ APPILES / bin / git
     $ git

 (Note)
The script 'termux.cmd.sh' uses `sed` to get the command name from the filename. If it does not work, please rewrite the command prompt part of termux.cmd.sh appropriately.

# 

**// Google translated from termux.txt located in same directory as this file from the original Japanese. //**
