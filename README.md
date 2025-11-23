# exz
AppImages on a budget
```
testofexz on  main 
-> # i have this neat pypy appimage: (made with https://files.obsidianos.xyz/~odd/pypy.sh)

testofexz on  main 
-> ./pypy.AppImage 
Python 3.11.13 (413c9b7f57f5, Jul 03 2025, 18:03:56)
[PyPy 7.3.20 with GCC 10.2.1 20210130 (Red Hat 10.2.1-11)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>> # it works
>>>> exit()

testofexz on  main took 5s 
-> # i want it as an exz.

testofexz on  main 
-> # first, this is the automatic method:

testofexz on  main 
-> ./appimage-to-exz pypy.AppImage 
Created inner tar.xz: /tmp/tmpwt75kpq2
Created outer tar containing compressed payload: /tmp/tmpqt2d8b08
Nested self-extracting script created: /home/odd/testofexz/pypy.exz

testofexz on  main took 7s 
-> ./pypy.exz
Python 3.11.13 (413c9b7f57f5, Jul 03 2025, 18:03:56)
[PyPy 7.3.20 with GCC 10.2.1 20210130 (Red Hat 10.2.1-11)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>> # it still works
>>>> exit()

testofexz on  main took 8s 
-> rm pypy.exz # now time to make it manually

testofexz on  main 
-> ls
LICENSE  README.md  appimage-to-exz  exz-maker  pypy.AppImage

testofexz on  main 
-> ./pypy.AppImage --appimage-extract

testofexz on  main 
-> ./exz-maker squashfs-root AppRun pypy.exz
Created inner tar.xz: /tmp/tmpvdkfqfk7
Created outer tar containing compressed payload: /tmp/tmpk7kcm2xw
Nested self-extracting script created: /home/odd/testofexz/pypy.exz

testofexz on  main took 8s 
-> rm -rf squashfs-root 

testofexz on  main 
-> ./pypy.exz 
Python 3.11.13 (413c9b7f57f5, Jul 03 2025, 18:03:56)
[PyPy 7.3.20 with GCC 10.2.1 20210130 (Red Hat 10.2.1-11)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>> # it works this way too
>>>> exit()
```
