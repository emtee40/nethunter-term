### Use terminfo on android

 Copy the included terminfo directory to a suitable location on android.
 However, directory names starting with a capital letter under terminfo should have l added like `al`.
 It has been saved.
 This is for the case of decompressing on a case-insensitive system such as windows.
 Because it is.

 Therefore, when using on android, the directory starting with a capital letter is the directory with l removed.
 You need to change it to a bird name.

     terminfo / al → terminfo / a


   (Setting Example)
   Register the following in "Settings"-> "Initial command" of android terminal emulator.

     export terminfo = / path / to / terminfo
     export term = screen-256color

   * In the setting example, it is assumed that terminfo is copied to / path / to / terminfo.
   * In android terminal emulator in / path / to
     It's a good idea to use /data/data/jackpal.androidterm.

 ### Create terminfo with windows (cygwin).

 If you ./configure and make ncurses from cygwin, it will be created in / usr / share / terminfo.

   * http://www.gnu.org/software/ncurses

 However, the directory name under terminfo is represented by the numerical value (hexadecimal) of the character code such as `33`.
 It has been.
 This is because, unlike Windows, file names are case sensitive in unix.

 Therefore, when using it on android, it is case-sensitive, as shown in the following example.
 You need to change the bird name.

     terminfo / 53 → terminfo / S
     terminfo / 73 → terminfo / s
   

**// Google translation from terminfo.txt included in terminfo.zip file from the original Japanese. //**
