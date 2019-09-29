#ricing

##Useful Resources
                        <li><a href="https://www.reddit.com/r/unixporn//a/">r/UnixPorn</a></li>
                        <li><a href="https://www.reddit.com/r/wallpapers/">r/wallpapers</a></li>
                        <li><a href="http://boards.4chan.org/wg/thread/7449335#p7449335/">Firefox CSS customization</a></li>
                        <li><a href="https://www.youtube.com/user/dubbeltumme">Budlabs</a></li>
###Description
<p1>This is broken down to folders named months. I rice my desktop on a monthly basis hence the month naming
Anyway lets get to busines

###Tools of The trade

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

# start dmenu (a program launcher)
bindsym $mod+d exec dmenu_run
           
         *Unfinished
