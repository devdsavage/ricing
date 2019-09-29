# ricing

## Useful Resources

[UnixPorn](https://www.reddit.com/r/unixporn)

[r/wallpapers](https://www.reddit.com)

[Firefox CSS customization](http://boards.4chan.org/wg/thread/7449335#p7449335/)

[Budlabs](https://www.youtube.com/user/dubbeltumme)

### Description
<p1>This is broken down to folders named months. I rice my desktop on a monthly basis hence the month naming
Anyway lets get to busines

### Tools of The trade

There are a couple of things you need to be able to rice . I might not get everything correct so pardon me
First you need an Operating System. 
  
If you are not sure on which Linux Os to go with you can check this <a href="https://i.imgur.com/wXsA1Ls.jpg">guide.</a>
We will be using manjaro in this guide  as it comes with a handy gui installer. Feel adventurous? install arch

First Tool is Rofi. rofi is an application launcher that we will use to get rid of dmenu.
you can find it from the Aur and can be installed with the following command 
```
sudo pacman -S rofi
```
Once its done we have to make a few changes to our i3 config. In a terminal type 
```
nano ~/.i3/config
```
and replace the lines
```
#start dmenu (a program launcher)
bindsym $mod+d exec dmenu_run
```
with 
```
#launch application via rofi
bindsym $mod+d exec --no-startup-id rofi -show drun
```
For further Configuration we can edit our rofi config  `~/.config/rofi/config.rasi`

if it doesnt exist create the folder and file accordingly.

Replace what's in the file with
```
configuration {
    display-run:                   "programs";
    display-window:                 "windows";
    display-ssh:                    "ssh";
    show-icons:                     true;
    icon-theme:                     "Adwaita";
}
 
* {
    lines: 15;
    columns: 1;
    background-color: #00000065;
    border-color: #00000000;
    text-color: #EFEFEF;
    font: "Hack 11";
}
 
#window {
    border: 0;
    border-radius: 4px;
    padding: 30;
    width: 40%;
    height: 60%;
}
 
#mainbox {
    background-color: #00000000;
    children: [inputbar, listview];
    spacing: 15px;
    /*margin: 20%;*/
    padding: 7px 0;
    border: 1px;
    border-color: @base0D;
}
 
 
#listview {
    background-color: #00000000;
    fixed-height: 0;
    border: 0px;
    spacing: 5px;
    scrollbar: false;
    padding: 10px 10px 0px;
}
 
#element {
    background-color: #00000000;
    border: 0;
    border-radius: 15px;
    padding: 3 0 3 4 ;
}
 
#element selected {
    background-color: #00a0e6;
    text-color: #EFEFEF;
}
 
 
#inputbar {
    children:   [ prompt,textbox-prompt-colon,entry,case-indicator ];
    background-color: #00000000;
}
 
#case-indicator {
    background-color: #00000000;
    spacing:    0;
}
#entry {
    background-color: #00000000;
    spacing:    0;
}
#prompt {
    background-color: #00000000;
    spacing:    0;
}
 
#textbox-prompt-colon {
    background-color: #00000000;
    expand:     false;
    str:        ":";
    margin:     0px 0.3em 0em 0em ;
}
```



           
         *Unfinished
