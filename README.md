# DO

- working on adding chrome theme generation

# KDE wallpaper randomizer

a small bash script that pick a wallpaper from a provided directory sets it on all monitors, sets kde style(shading colors, folder colors, etc.), and uses pywal to generate a konsole colorscheme and sets it.

## Acknowlegments

Thanks to these two post for helping me create this script.
<https://superuser.com/questions/488232/how-to-set-kde-desktop-wallpaper-from-command-line>
<https://superuser.com/questions/1193957/how-can-i-change-the-colorscheme-through-command-line>
You can see the code that I copied there.

## requirements 

1. kde x11 (have not tested on wayland results may vary)
2. wget
3. [pywal](https://github.com/dylanaraps/pywal/wiki/Installation)

## Installaiton

```sh
cd .local/bin
wget https://github.com/nate0m/kde-wallpaper-randomizer/blob/main/new-look
chmod +x new-look 
```
add .local/bin to your path if you have not already
```sh 
vim ~/.bashrc
export PATH="$PATH:/home/username/.local/bin"
```
replace bash with zsh if you use zsh

apply changes
```sh
source ~/.bashrc
```

## Usage
There are two ways to run the script. One by passing the absolute path to the wallpaper you want, and two not passing anything and the script will pick randomly from the directory of wallpapers you provide.

add the path to your wallpapers
```sh
vim .local/bin/new-look
```
change the `location` variable to your wallpapers directory's absolute path.

you can also change the transperancy of konsole by editing the number on line 53. 1 = solid.

## Closing Thoughts
This script will proably be broken by some change to pywal in the future because of the hacky way that I am chaning the opacity by editing the specific line in the file. If you don't care about tranperancy you can remove that entire block. Otherwise `¯\_(ツ)_/¯`



