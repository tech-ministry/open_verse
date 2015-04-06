PyQt5 Installation inside virtualenv (Python 3.4)
==================================

## Instructions for OS X

* Install Xcode
* install the Command Line Tools (open Xcode > Preferences > Downloads)
* install Qt libraries (qt-opensource-mac-x64-clang-5.2.1.dmg)
* Install Homebrew: ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
* brew update (to update the list of formulas)
* brew install python3
* pyvenv /path/for/your/new/venv
* unzip and compile SIP and PyQt

```
    cd /var/tmp
    cp /Users/your_user/Downloads/PyQt-gpl-5.2.1.tar.gz .
    cp /Users/your_user/Downloads/sip-4.15.5.tar.gz .
    tar xvf PyQt-gpl-5.2.1.tar.gz
    tar xvf sip-4.15.5.tar.gz
    cd sip-4.15.5/
    python3 configure.py -d ~/.env/ariane_mail/lib/python3.4/site-packages --arch x86_64
    make
    sudo make install
    sudo make clean
    cd ../PyQt-gpl-5.2.1/
    python3 configure.py --destdir ~/.env/ariane_mail/lib/python3.4/site-packages --qmake ~/Qt5.2.1/5.2.1/clang_64/bin/qmake
    make
    sudo make install
    sudo make clean
    ~/.env/ariane_mail/bin/python -c "import PyQt5"
```

