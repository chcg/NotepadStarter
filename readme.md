##Introduction
This tool designed as a Notepad++ plugin by luoyonggang(at)gmail.com, when it installed as
a Notepad++ plugin or running NotepadStarter.exe in the Notepad++ app directory, it's will
automatically replace the system default notepad.exe application with Notepad++ (Without
need for removing anything from the windows system.).  It's tested under Windows 7, but
Windows XP should also works.

This tool is based on the sources from npplauncher by [Stepho,2005](http://superstepho.free.fr/)
and [mattesh(at)gmx.net,2013] (http://sourceforge.net/projects/npplauncher/).

##Design
NotepadStarter make use of a debugger feature in Windows the system will call a hooked 
process with appended parameters to allow debugging the intended application.
This hook application will be call whenever the correct application was resolved.
  
notepad.exe receives always only one parameter which is now just deferred to Notepad++.
Because notepad.exe is a blocking executable, so NotepadStarter behaves blocking as notepad.exe.
Notepad++ have multiple tab page, so NotepadStarter will terminated when the corresponding
tab page closed or the corresponding Notepad++ application is closed.

##Contributions
Comments, issues and contributions can be done at [Github|NotepadStarter](https://github.com/lygstate/notepadstarter)