# MD�ļ���д[��ʽ](https://blog.csdn.net/carcarrot/article/details/119769300)

# ���� WSL �� ubuntu22.04 ���� flair��
## Locate to the program directory��
    cd /mnt/d/xinwenir/PostDoctor/Nuclear_Science/FLUKA/flair-geoviewer-2.3-main

# ��װ tkinter

## ���� apt ��װ��

    sudo apt-get install python3-tk

## ���ֱ���

    File "/usr/local/python3.8/lib/python3.8/tkinter/__init__.py", line 36, in <module>                                   
        import _tkinter # If this fails your Python may not be configured for Tk                                            
    ModuleNotFoundError: No module named '_tkinter' 

����Ŀ¼��

    sudo mkdir /usr/local/lib/python3.8/lib-dynload

�����ļ���

    cd /usr/lib/python3.8/lib-dynload
    cp 



# [tk/tcl�İ�װ](https://blog.csdn.net/RadiantJeral/article/details/108021607)

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


# Install python3.8.10: 

** �ο�[����](https://blog.csdn.net/weixin_46584887/article/details/120701003)

## һ��apt ��װ���������

ִ�������������Դ��

    sudo apt-get update

ִ���������װ Python3 ��һЩ�����⣺

    sudo apt-get install libqgispython3.10.4
    sudo apt-get install libpython3.10-stdlib


## ��������Դ���

��ҿ���ǰ�� Python �������أ�Welcome to Pyhton! ���������� gz ���� xz �������ԣ������������£�XZ compressed source tarball

Ҳ��ʹ�� wget ���أ�ѡһ�ַ������ɣ�

    wget -P ~/Downloads https://www.python.org/ftp/python/3.8.10/Python-3.8.10.tar.xz


���Ž�ѹ tar ����

    cd ~/Downloads
    tar xvJf Python-3.8.10.tar.xz

    
���ˣ�׼����������������

## ����Դ�����װ Python3.10.8
### 1. ���밲װ
���Ƚ������ǸղŽ�ѹ���ļ�Ŀ¼�£�

    cd ~/Downloads/Python-3.10.8

��װ GCC��������

    sudo apt-get install gcc

���ñ��������������ļ�Ŀ¼��

    ./configure --prefix=/usr/local/python3.8

��װ GCC��������

    sudo apt-get install make

����ʵʩ���룺

    make
��װ pip��

    sudo apt-get install pip

�������������д��������������Ҫ�ȴ��������ӣ�������ɺ�װ��

    sudo make install


�����������������˵����װ�ɹ���

    Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
    Successfully installed pip-21.2.3 setuptools-57.4.0
    WARNING: Running pip as the ��root�� user can result in broken permissions and conflicting behaviour with the system package      manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv


### 2. ����������
��һ���������ǵ� python �����ܹ����ӵ������°�װ�� Python3.10.0 ��ִ�г�������Ǹ��͵İ汾���������Ƚ��뵽 /usr/bin Ŀ¼�£�

    cd /usr/bin

��������������Բ鿴 Python ����֮ǰ�����������

    ll | grep python

�� Ubuntu �£�ϵͳĬ���ǰ�װ�� Python2.7 �汾�ģ������ҵĵ����� python �����Ƕ�Ӧ Python2.7 �汾���� python3 ������Ƕ�Ӧ�� Python3* �汾�������������������޸ģ�

    sudo rm ./python # ɾ��ԭ�е��������ļ�
    sudo rm ./pip
    sudo rm ./pip3

�����������µ������ӵ����ǵ� Python3.10 �汾��

    sudo ln -s /usr/local/python3.8/bin/python3.8 /usr/bin/python
    sudo ln -s /usr/local/python3.8/bin/pip3.8 /usr/bin/pip
    sudo ln -s /usr/local/python3.8/bin/pip3.8 /usr/bin/pip3

ע���������ǲ��ܽ�ϵͳ�е� python3 �������ӵ� python3.10 �汾���������Ѿ��ȿӣ�����Ϊ python3.10 �汾���Ƿ��Ͱ汾���������ȶ��汾�������ĺ���ᵼ�� Ubuntu ϵͳ�µĺܶ� python �ļ��޷��򿪣�������� gnome �նˣ���

### 3. ����
��������������� Python �����Ƿ�ɹ���

    python -V

������£�

    zq@fzqs-computer:/usr/bin$ python -V
    Python 3.10.0

��������������� Python �����Ƿ�ɹ���

    pip3 -V

������£�

    zq@fzqs-computer:/usr/bin$ pip3 -V
    pip 21.2.3 from /usr/local/python3/lib/python3.10/site-packages/pip (python 3.10)

���������ǵ� Python3.10 �Ͱ�װ�����������

### 4. ���� pip ����
�ڰ�װ�������ֱ�������ִ�� pip list ���������Ҫ�޸� pip ����������ļ���

    sudo vim /usr/bin/lsb_release

�޸ĵ�һ�е� Python3 Ϊ Python3.10 ���ɣ�������ִ�� pip list ���

    zq@fzqs-computer:/usr/bin$ pip list
    Package Version
    - - - - - - - - - - - - -
    pip 21.2.3 setuptools 57.4.0

�����ȷ���󹤸�ɣ�

�ܽ�
match-case �������Ϊ Python ���﷨��������һ�ݶ��е������ɣ�������һ�� match-case ���룺

def http_error(status):
    match status:
        case 400:
            return "Bad request"
        case 401 | 402 | 403:
            return "Not allowed"
        case 404:
            return "Not found"
        case 418:
            return "I'm a teapot"
        case _:
            return "Something must be wrong!"