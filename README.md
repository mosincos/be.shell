Install [BE::Shell](http://sourceforge.net/p/be-shell/code/ci/master/tree/) or upgrade to the latest commit.
Themes are made with [QSS](http://qt-project.org/doc/qt-4.8/stylesheet-reference.html) - Qt Style Sheets, while the menu files for the globalmenu applet follow a simple [xml syntax](http://sourceforge.net/p/be-shell/wiki/Menu%20reference/).
Some of the menus, *Recent* and *Places*, are generated by the relative scripts located under the Scripts folder.

**Notes** 

- Due to the absolute positioning in BE::Shell themes may need adjustments within the css or the config file.
- The places script requires xmlstarlet

Installation
======

**Theme and Config**

Clone this repository:

    git clone https://github.com/Hombremaledicto/be.shell.git
    cd be.shell
    
You can either install using the provided script or copying the files manually.
   
**By script**

*Notice!* The script does not install menus and scripts, check the section below for them!

    chmod 777 install
    ./install
    
Or, alternatively, you can skip the list of available presets and specify directly the one you want, passing its name after the -p argument - e.g. for be.shell.Vertex :

    ./install -p Vertex
    
*Note* By default the script will ask if you want to backup your current config and theme, this functionality can also be invoked with:

    ./install -b
    
 **Manually**
 
If this is the first time you install BE::Shell, you need to create its configuration and themes folders:

    mkdir -p `kde4-config --localprefix`/share/apps/be.shell/Themes
 
Copy the Theme directory: 

    cp -r Themes `kde4-config --localprefix`/share/apps/be.shell/

Copy the included config file (for example be.shell.Vertex) as be.shell:

    cp be.shell.Vertex `kde4-config --localprefix`/share/config/be.shell
   
If you're using Plasma, kill it and start BE::Shell:

    kquitapp plasma-desktop; sleep 2; be.shell
    
If you're already on BE::Shell, restart it in order to apply the new theme & config:

    be.shell --restart
   
   
**Menus & scripts** 

Copy the folders Menu, Scripts and the MainMenu.xml file:

    cp -R Menu Scripts MainMenu.xml `kde4-config --localprefix`/share/apps/be.shell
  
Make the scripts executable:

    chmod -R 777 `kde4-config --localprefix`/share/apps/be.shell/Scripts/*


Vertex
======

Unity-Like dark theme using [BE--Tray icons](http://be-desk.deviantart.com/art/Be-Tray-Icons-16px-364645083) by LaGaDesk and [Moka Minimal](http://cbowman57.deviantart.com/art/Moka-Minimal-and-Faba-Minimal-Icon-Sets-482927307) by cbowman57.
The suite is inspired by [Vertex GTK](http://horst3180.deviantart.com/art/Vertex-Theme-470663601).


![Vertex preview](https://lh5.googleusercontent.com/-h83zA_HCRVQ/VGYMxGGvQOI/AAAAAAAAC7I/eNZRGMB8qW4/w1058-h595-no/schermata662.png "Vertex")

Dynamo
======

A light theme miming the official Breeze artworks for KDE Plasma5. You can find the offial Breeze icon theme [here](https://github.com/NitruxSA/plasma-next-icons).
Dynamo makes use of BE::Shell labels, either by polling a script, either as FiFos. Some of these scripts are included in this repository (check the Scripts folder for rss2html and be.kdeconnect), others are from [magpie240](https://github.com/magpie240) and require to be installed & configured from the relative repositories:

- [shellfeed](https://github.com/magpie240/shellfeed)
- [shelloid_mpris](https://github.com/magpie240/shelloid_mpris)

![Dynamo preview](https://raw.githubusercontent.com/Hombremaledicto/be.shell/master/Pictures/Dynamo.png "Dynamo")

Pandora
======

Mac alike preset directly derived from Dynamo.
*Coming Soon*

![Pandora preview](https://raw.githubusercontent.com/Hombremaledicto/be.shell/master/Pictures/Pandora.png "Pandora")
