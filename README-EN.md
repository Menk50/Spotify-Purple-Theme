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

Config 
Theme


<h3>Config</h3>
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
 
 <h3 > <a href="https://github.com/Menk50/Spotify-Purple-Theme/"> Themes</a> </h3>
 
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
