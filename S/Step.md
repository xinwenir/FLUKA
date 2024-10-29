# VS-Code ��װ�� WSL��

## �� WSL �µ� Ubuntu ϵͳ��

    code ..

# MD�ļ���д[��ʽ](https://blog.csdn.net/carcarrot/article/details/119769300)

# ���� WSL �� ubuntu22.04 ���� flair��
## Locate to the program directory��
    cd /mnt/d/xinwenir/PostDoctor/Nuclear_Science/FLUKA/flair-geoviewer-2.3-main

# ��װ python

    sudo apt-get install python3-dev

Point the "python" command to python3."

    sudo ln -s /usr/bin/python3 /usr/bin/python

Point the "python-config" command to python3-config."

    sudo ln -s /usr/bin/python3-config /usr/bin/python-config
    
# ��װ tkinter

## ���� apt ��װ��

    sudo apt-get install python3-tk

## ����

    python
    import tkinter
    tkinter._test()

## ���ִ���

    File "/usr/local/python3.8/lib/python3.8/tkinter/__init__.py", line 36, in <module>                                   
        import _tkinter # If this fails your Python may not be configured for Tk                                            
    ModuleNotFoundError: No module named '_tkinter' 

 - ����Ŀ¼��

        sudo mkdir /usr/local/lib/python3.8/lib-dynload


 - �����ļ���

        cd /usr/lib/python3.8/lib-dynload
        cp 



# [tk/tcl�İ�װ]

����[tk/tcl](http://www.tcl.tk/software/tcltk/download.html)

    tar ��zvxf tclxxx.tar.gz
    cd tclxxx/unix
    ./configure
    make
    sudo make install

    tar ��zvxf tkxxx.tar.gz
    cd tkxxx/unix
    ./configure
    make
    sudo make install


# FLUKA��װ
64 bits, Linux, requires gcc/gfortran (version >=9.4)
  - Linux x86_64 (tar.gz packages): fluka2024.1-linux-gfor64bit-yy-glibczzAA.tar.gz fluka2024.1-data.tar.gz  

���غ�������£�

    mkdir /home/zxw/fluka
    export FLUPRO=/home/zxw/fluka
    sudo apt install gfortran
    export FLUFOR=gfortran
    cp fluka2024.1-linux-gfor64bit-yy-glibczzAA.tar.gz $FLUPRO
    tar -zxvf fluka2024.1-linux-gfor64bit-yy-glibczzAA.tar.gz
    make

    nano ~/.bashrc

��ӣ�

    export FLUPRO=/home/zxw/fluka
    export FLUFOR=gfortran







# �ҵ�X11/Xlib.h��

    sudo apt-get install libx11-dev

# win11ж��Ubuntu 20.04 WSL ��[����](https://blog.csdn.net/bmseven/article/details/129365761)

## ͨ��Windows�ն�ж��
### 1���鿴��ǰ������װ��wsl

    wsl --list

### 2��ע����ж�أ���ǰ��װ��Linux��Windows��ϵͳ������Ҫ��list��ȡ��һ�£�

    wsl --unregister Ubuntu-20.04

### 3��ж�سɹ����鿴��ǰ��װ��Linux��Windows��ϵͳ

    wsl --list


# ж��python3.8

## ж��python3.8��

    sudo apt-get remove python3.8

## ж��python3.8����������

    sudo apt-get remove --auto-remove python3.8

## ���python3.8��

    sudo apt-get purge --auto-remove python3.8

