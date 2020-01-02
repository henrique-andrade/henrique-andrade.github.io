# Installing gretl for dummies

## elementary OS

### Initial setup

Open the **Terminal** app and enter the command

```bash
sudo pico /etc/apt/sources.list
```

Remove the "#" from the line above

```
deb-src http://br.archive.ubuntu.com/ubuntu/ bionic universe
```

Enter the command to update your package repositories

```
sudo apt update
```

### Installing dependencies

Install the packages you need to build **gretl**. Again using **Terminal** enter the following commands

```bash
sudo apt install git
sudo apt install texlive-full
sudo apt build-dep gretl
```

### Donwloading gretl's files

```bash
# Alternative 1
git clone git://git.code.sf.net/p/gretl/git ~/gretl/git
```

If that command doesn't work (due to some network restrictions), you can try this alternative

```bash
# Alternative 2
git clone https://git.code.sf.net/p/gretl/git ~/gretl/git
```

That commands (alternatives 1 or 2) will download all necessary files and save them in the folder named `git` inside `gretl` located at you home folder.

### Installation

After these steps you need to go to that new directory

```bash
cd ~/gretl/git
```

And then, finally you just need to enter the following commands

```bash
./configure --enable-build-doc --enable-build-addons  
make  
sudo make install  
cd ~  
sudo ldconfig  
```

Now you have **gretl** installed and accesible under the Applications menu in elementary OS.

### Updating 

To keep your **gretl**'s installation up to date you just need to open **Terminal** and run the following commands:

```bash
cd ~/gretl/git  
git pull  
./configure --enable-build-doc --enable-build-addons --with-odbc  
make  
sudo make install 
sudo ldconfig
```

## Linux Mint

## Manjaro

## Ubuntu

## Pop!_OS