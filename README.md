# ConEmu Setup Tutorial
Setup ConEmu to run multiple windows for development.

1. Install ConEmu
2. Go to settings (Win + Alt + p)
3. Go to `Startup => Tasks`
4. Click `Add/refresh default tasks => Add new tasks`
5. Click on new predefined task and put the following into the console on the right
````
powershell -cur_console:n

powershell -cur_console:s1TVn

set "PATH=%ConEmuDir%\..\Git\usr\bin;%PATH%" & "%ConEmuDir%\..\Git\git-cmd.exe" --no-cd --command=%ConEmuBaseDirShort%\conemu-msys2-64.exe /usr/bin/bash.exe -l -i -cur_console:s1THn

powershell  -cur_console:s2THn
````
6. Go back to `Startup` tab and select the new named task
7. Save settings

Now close + open ConEmu. You should see 3 powershell windows and 1 git bash window.
