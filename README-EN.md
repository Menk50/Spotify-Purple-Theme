# Spotify Purple Theme
If you are tired of the default Spotify theme, this is for you

<h3>Spotify InterFace Demo</h3>
 <img Src="https://github.com/Menk50/Spotify-Purple-Theme/blob/master/Demo.png?raw=true" widht="490" height="350" alt="Spotify InterFace Demo" >
<h1>#Install</h1>
 
<h5>Step 1</h3> 
<ul>
 <li> <a href="https://github.com/khanhas/spicetify-cli/wiki/Installation#with-powershell-pre-built-binary"> Spicetify-cli Download</a> </li>
</ul>


<h1> Customization </h1>

<a href="#config">Config </a> <br>
<a href="#themes">Theme </a>


<h3 > <a name="config">Config</a></h3>
Config file is located at:

<b>Windows</b>:
```     %userprofile%\.spicetify\config.ini ```
 
<b>Linux</b>: ``` $XDG_CONFIG_HOME/.config/spicetify/config.ini or ~/.config/spicetify/config.ini ```

<b>MacOS</b>: 
``` ~/spicetify_data/config.ini ```

Or simply run
 ```spicetify -c ```
 to know where it is.

For detail information of each config field, please run:
 
 ``` spicetify --help config  ``` 
 
 <h3 > <a name="themes"> Themes</a> </h3>
 
 There are 2 places you can put your themes:
 

  ``` Themes  ``` folder in Home directory 

  
  <b>Windows</b>:
```     %userprofile%\.spicetify\Themes\ ```
 
<b>Linux</b>: ``` $XDG_CONFIG_HOME/.config/spicetify/Themes/ or ~/.config/spicetify/Themes ```

<b>MacOS</b>: 
``` ~/spicetify_data/Themes ```

``` Themes  ``` folder in Spicetify executable directory 



If there are 2 themes having same name, theme in Home directory is prioritized.

Every theme should contain: 

```color.ini: ```store colors value that later will be converted to CSS variables
```user.css:``` set of custom CSS rules to manipulate, hide, move UI elements.
Color value can be in several formats and forms:

Hex: e.g ```#FF0000```, ```#1258F6```, ```#F55```

Decimal: e.g ```255,255,255```, ```50,80,120```

Environment variables can be used in place of color.

Syntax: ```${<variable name>}```
Example usage: ```main_fg = ${LIGHT_GREY}```
[Linux] You can use XResources variable in place of color. Extremely useful for who uses pywal to generate color scheme.

Syntax:``` ${xrdb:<variable name>} ```or ```${xrdb:<variable name>:<fallback value>}```
Example usage:
```
[Base]
main_fg       = ${xrdb:color14}
secondary_fg  = ${xrdb:foreground:#FFF}
main_bg       = ${xrdb:background}
```

<h3>How to install Theme</h3>

Run these command

<b>Linux and MacOS:</b>
In <b>Bash</b>:

```cd "$(dirname "$(spicetify -c)")/Themes/Dribbblish"
cp dribbblish.js ../../Extensions
spicetify config extensions dribbblish.js
spicetify config current_theme Dribbblish color_scheme base
spicetify config inject_css 1 replace_colors 1 overwrite_assets 1
spicetify apply
```
<b>Windows</b>
In <b>Powershell:</b>

```cd "$(spicetify -c | Split-Path)\Themes\Dribbblish"
Copy-Item dribbblish.js ..\..\Extensions
spicetify config extensions dribbblish.js
spicetify config current_theme Dribbblish color_scheme base
spicetify config inject_css 1 replace_colors 1 overwrite_assets 1
spicetify apply
```

</h3>Hide Window Controls</h3>
Windows user, please edit your Spotify shortcut and add flag ```--transparent-window-controls``` after the Spotify.exe:

<img src="https://github.com/Menk50/Spotify-Purple-Theme/blob/master/Capture.PNG?raw=true" alt="transparent-windows-controls">

Alternatively, you can use ```SpotifyNoControl.exe```, included in this theme package, to completely remove all windows controls and title menu (three dot at top left corner). Title menu still can be access via Alt key. Closing, minimizing can be done via right click menu at top window region.
```SpotifyNoControl.exe``` could be used as Spotify launcher, it opens Spotify and hides controls right after. So you should make a shortcut for it, change icon and add to desktop or start menu.
Moreover, by default, Spotify adjusted sidebar items and profile menu icon to stay out of Windows native controls region. If you decided to use ```SpotifyNoControl.exe``` from now on, please open ```user.css``` file and change variable -```-os-windows-icon-dodge``` value to 0 as instruction to snap icons back to their original position.

<img src="https://github.com/Menk50/Spotify-Purple-Theme/blob/master/Capture2.PNG?raw=true" alt="transparent-icon">

<h3>Extra Color Schemes</h3>
There are 1 color chart you can choose, you can clone it and create it as you want. By default, there is a ```Purple``` Color chart.
```
spicetify config color_scheme <scheme name>
spicetify apply
 ```
 
<code>color.ini</code>  reference 
 These keys are used in the ```colors.ini ``` file.
 
 <img src="https://github.com/Menk50/Spotify-Purple-Theme/blob/master/color.PNG?raw=true" alt="color.ini">
