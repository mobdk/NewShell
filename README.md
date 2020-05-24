# NewShell
Reverse shell without Windows cmd.exe, using ReactOS cmd.dll as shellcode
Using Windows cmd.exe when spawn a revers shell works fine, but in some cases cmd.exe is blocked by GPO or other security produkt like EDR's, I have created this to bypass this restrictions and using ReactOS cmd.dll converted to shellcode. ReactOS's cmd.dll can without any problem be spawned with CreateProcess, where cmd.dll exist as file.

Use MSBuild.exe to compile, Visual Studio don't handle large arrays very well.
Compile: MSBuild.exe /p:Platform=x86 newshell.vcxproj
Execute newshell.dll,shell
