# rtl8821cu-5.4.1-kernel-5.0
8811cu,8821cu chip linux driver 0bda:c811
source from realtek, maybe work for above chips for the newest linux kernel 4.19-5.0. 
tested it works on fedora 29 workstation.
tenda U9, DWA-17C, Mercury UD6 etc may work.
linux kernel 5.0 remove VLA, original source files contain VLAs, this drv just:
1) add "-Wno-vla" to Makefile to supress warnings, and 
2) change a function parameters in os_dep/linux/rtw_android.c search or access_ok to modified before compiling.
better wait for realtek to release new. but just work fine.
