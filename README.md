# Friday Night Funkin 11O1 ENGINE!

Friday Night Funkin, is a rhythm game originally made for Ludum Dare 47 "Stuck In a Loop".

## Credits / shoutouts

- [ninjamuffin99](https://twitter.com/ninja_muffin99) - Programmer
- [PhantomArcade3K](https://twitter.com/phantomarcade3k) and [Evilsk8r](https://twitter.com/evilsk8r) - Art
- [Kawaisprite](https://twitter.com/kawaisprite) - Musician
- [JovaDeveloper(me!)](https://twitter.com/JDevTheGod) -Compiler

Welcome to Funkin11O1 an engine that has compiled older versions of FNF!

Funkin11O1 Is an engine that revisits some of the older versions of Friday Night Funkin'.

![screenshot__yepirenamedit](https://user-images.githubusercontent.com/86385501/216802032-805d7c56-7881-41db-baf9-12e7c3eb9350.png)


## Build instructions

THESE INSTRUCTIONS ARE FOR COMPILING THE GAME'S SOURCE CODE!!!

If you just want to play the game then go to the Gamebanana Page! Its for MACOS and Windows!

(https://gamebanana.com/mods/425933)

If you want to compile it yourself go right ahead and keep reading!

also there is a txt file for information about 0.1.0 and 1.0.0 ALSO information to install 0.2.0!

### Installing the Required Programs

First, you need to install Haxe and HaxeFlixel!
1. [Install Haxe 4.1.5](https://haxe.org/download/version/4.1.5/) (Download 4.1.5 instead of 4.2.0 because 4.2.0 is broken and is not working with gits properly...)
2. [Install HaxeFlixel](https://haxeflixel.com/documentation/install-haxeflixel/) after downloading Haxe

Other installations you'd need are the additional libraries, a fully updated list will be in `Project.xml` in the project root. Currently, these are all of the things you need to install:
```
haxelib install flixel <---- If it saying UpdateFrgament Shit then install 4.11.0
haxelib install flixel-addons
haxelib install flixel-ui
haxelib install hscript
haxelib install newgrounds 1.2.0
```
THE REASON WHY YOU HAVE TO INSTALL OLDER VERSION OF NEWGROUNDS BECAUSE: Other Versions uses other versions of newgrounds so it will get fucked up if you use another version.

You'll also need to install a couple things that involve Gits. To do this, you need to do a few things first.
1. Download [git-scm](https://git-scm.com/downloads). Works for Windows, Mac, and Linux, just select your build.
2. Follow instructions to install the application properly.
3. Run `haxelib git polymod https://github.com/larsiusprime/polymod.git` to install Polymod.
4. Run `haxelib git discord_rpc https://github.com/Aidan63/linc_discord-rpc` to install Discord RPC.

You should have everything ready for compiling the game! Follow the guide below to continue!

At the moment, you can optionally fix the transition bug in songs with zoomed-out cameras.
- Run `haxelib git flixel-addons https://github.com/HaxeFlixel/flixel-addons` in the terminal/command-prompt.

### Ignored files

I gitignore the API keys for the game so that no one can nab them and post fake high scores on the leaderboards. But because of that the game
doesn't compile without it.

### DISCLAIMER

ONLY 0.2.1 AND THE REST USES APISTUFF!!
The others like 0.1.0 and 0.2.0 doesn't!

make a file in `/source` and call it `APIStuff.hx`, and copy & paste this into it

```haxe
package;

class APIStuff
{
	inline public static var API:String = "51348:TtzK0rZ8";
	inline public static var EncKey:String = "5NqKsSVSNKHbF9fPgZPqPg==";
}

```

and you should be good to go there.

### Compiling game
NOTE: If you see any messages relating to deprecated packages, ignore them. They're just warnings that don't affect compiling

Once you have all those installed, it's pretty easy to compile the game. You just need to run `lime test html5 -debug` in the root of the project to build and run the HTML5 version. (command prompt navigation guide can be found here: [https://ninjamuffin99.newgrounds.com/news/post/1090480](https://ninjamuffin99.newgrounds.com/news/post/1090480))
To run it from your desktop (Windows, Mac, Linux) it can be a bit more involved. For Linux, you only need to open a terminal in the project directory and run `lime test linux -debug` and then run the executable file in export/release/linux/bin. For Windows, you need to install Visual Studio Community 2019. While installing VSC, don't click on any of the options to install workloads. Instead, go to the individual components tab and choose the following:
* MSVC v142 - VS 2019 C++ x64/x86 build tools
* Windows SDK (10.0.17763.0)
For MacOS you can install Visual Studio Code or Visual Studio

Once that is done you can open up a command line in the project's directory and run `lime test windows -debug`. Once that command finishes (it takes forever even on a higher end PC), you can run FNF from the .exe file under export\release\windows\bin
As for Mac, 'lime test mac -debug' you can run the app file under export\release\macos\bin

### Additional guides

- [Command line basics](https://ninjamuffin99.newgrounds.com/news/post/1090480)
