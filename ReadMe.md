```
_|_|_|    _|    _|  _|      _|    _|_|_|  _|_|_|_|    _|_|    _|      _|                    _|_|      _|_|_|      _|_|      _|_|    _|      _|  
_|    _|  _|    _|  _|_|    _|  _|        _|        _|    _|  _|_|    _|        _|_|      _|          _|    _|  _|    _|  _|    _|  _|_|  _|_|  
_|    _|  _|    _|  _|  _|  _|  _|  _|_|  _|_|_|    _|    _|  _|  _|  _|      _|    _|  _|_|_|_|      _|    _|  _|    _|  _|    _|  _|  _|  _|  
_|    _|  _|    _|  _|    _|_|  _|    _|  _|        _|    _|  _|    _|_|      _|    _|    _|          _|    _|  _|    _|  _|    _|  _|      _|  
_|_|_|      _|_|    _|      _|    _|_|_|  _|_|_|_|    _|_|    _|      _|        _|_|      _|          _|_|_|      _|_|      _|_|    _|      _|  
_______________ _  _____ 
|__/|___|__||  \|\/||___ 
|  \|___|  ||__/|  ||___ 
```
> (
This project was the final coursework of the `Principles of Programming` Computer Science module I followed at the University of Bath.  
It is a fun (and dare I say, actually sort of claustrophobia-/fear-inducing) command-line-based game where you explore a dungeon and have to watch out not to be killed by a bot.  
I poured lots of passion into it and even went so far as to figure out Dijkstra's algorithm for pathfinding :)  
(And my hard work paid off, as I got basically the equivalent of a 100% as a grade~)  
I would consider this code base a good example of how ordered I like (my/anyone's) code to look if I have the time to spend on documenting/refactoring.
)

## Demo

![gif-2](/readme-images/dod-2.gif)  
![gif-3](/readme-images/dod-3.gif)  
![gif-4](/readme-images/dod-4.gif)

Thanks for trying out ***Dungeon of Doom***, a fun text-based adventure game where you loot dungeons while trying not to get caught!!  
Down below you will find all the necessary info to get started and to dive deeper.
Enjoy!
---

```
 _____             _          _  _         _    _               
|_   _|           | |        | || |       | |  (_)              
  | |  _ __   ___ | |_  __ _ | || |  __ _ | |_  _   ___   _ __  
  | | | '_ \ / __|| __|/ _` || || | / _` || __|| | / _ \ | '_ \ 
 _| |_| | | |\__ \| |_| (_| || || || (_| || |_ | || (_) || | | |
 \___/|_| |_||___/ \__|\__,_||_||_| \__,_| \__||_| \___/ |_| |_|
                                                                
```
To get started, navigate in your Linux command line to the "Project" folder in the location where you extracted the .zip file of the game.  
Then firstly compile all the necessary code to run the game by typing "javac *.java", and you're ready to go!

Start the game by typing `java GameLogic` and have fun (/^▽^)/

To actually start playing your first map, just press Enter and everything will speak for itself.  
Instead of pressing right away you can also type the name of a map file (with or without the '.txt' at the end) to play that particular custom map.  
One map called example_map.txt has already been included, but it's very easy to make or find your own maps (see later on).  
On a side note: when you type a non-existing filename, the game will just create the same map as if you typed nothing.  
```
 _____                                                                   _ 
|  __ \                                                                 | |
| |  \/  __ _  _ __ ___    ___    _ __ ___    __ _  _ __   _   _   __ _ | |
| | __  / _` || '_ ` _ \  / _ \  | '_ ` _ \  / _` || '_ \ | | | | / _` || |
| |_\ \| (_| || | | | | ||  __/  | | | | | || (_| || | | || |_| || (_| || |
 \____/ \__,_||_| |_| |_| \___|  |_| |_| |_| \__,_||_| |_| \__,_| \__,_||_|
```

### HOW TO WIN

Winning is (at least seemingly) very simple: collect the gold and get to the exit of the dungeon!  
The dungeon that you have to collect the gold in is made up out of square tiles and you can only move up, down, left and right.  
  
When you start the game, the amount of gold required to win is displayed and you can always remind yourself later with the HELLO command (:  
Collect a GOLD tile when you find it using the PICKUP command, and when you've got enough gold move onto an EXIT tile to finish the game!  


### WATCH OUT

Watch out though, as there is a BOT of terror moving around the dungeon that's out to catch you!  
However, as it's dark the bot can see just as much as you can, so it doesn't have any edge over except that you cannot touch it by with even so much as a hair.  
And that it's got cool algorithms to hunt you down as efficiently as possible when it sees you.  
But anyways, you're smart so you'll be just fine!!  
Concretely put: when the bot ends up on the same tile as you, your dead. ಠ_ಠ  


### AVAILABLE ACTIONS

These are the available commands you can type during the game:
* `HELLO`\
	For some reason, when you greet the game it reminds you of you much gold you've left to collect to be able to finish the game.

* `LOOK`\
	It'd be boring if you could just see the entire map, right? Plus, dungeons are dark, so it's nice and mysterious.
	Anyways, this command is your only means to see during the game, and it shows you a 5x5 square of what's currently around you. You can of course still walk when you can't see anything, but tread carefully, and good luck not accidentally running into the bot ヽ(ﾟДﾟ)ﾉ
	Note that this is ALSO the only means to see for the bot, so it's all fair play.

* `MOVE <direction>`\
	If you want to move, you have to type in `MOVE`, followed by a wind direction. For instance, `MOVE S` moves you one tile to the SOUTH, which would mean 'down' on the map.
	Of course, if you try to move somewhere that's not possible (i.e. a wall), you won't be granted the divine priviledge to just do that anyways, so you'll just have wasted your turn!

* `PICKUP`\
	This is the command you use when you're on a gold tile and you want to pickup that juicy gold and show it where it belongs. If succesful, the gold you have will increase by 1 and the gold wil disappear from the tile.

* `QUIT`\
	Quits the game. Be careful not to accidentally type this when you've made some great progress.
	To quit the game there'sa also the shortcut Ctrl+D, so be even more careful not to press this by accident.

* `PASS`\
	Just don't do anything (pass your turn), as you let the bot slowly sneak up on you only to open your eyes and... ～ﾍ(ﾟдﾟﾍ))))))～

* `COMMANDS`\
	This prints out this very list of commands so you won't have to open up this txt file all the time, with your weak short term memory.

Do note that for any of these commands, it doesn't matter if you go upper/lowercase and it's also fine to put spaces beforehand/afterwards. Yeh, the game is flexible and robust like that!


### TILES YOU MAY SEE WHEN YOU `LOOK`

The following tiles may be displayed when you issue the LOOK command:
* `.` : SPACE\
	An empty space. You can easily move onto this.

* `P` : PLAYER\
	It's you! Don't get spooked by yourself!

* `#` : WALL\
	#wall #funny, anyways don't attempt to move into this as it will only result in disappointment.

* `G` : GOLD\
	Look at that, it's so shiny! Quick, pick it up before anyone else does!

* `E` : EXIT\
	When you got (more than) enough gold, move onto this tile to escape and let that horrible bot of terror rot for all it's worth.
	You can, by the way, easily move over it even if you don't have enough gold to bribe the doorguard.

* `B` : BOT\
	It's that scary fella again... Be careful not to lose your attention for even a second, as you'll get caught!

A useful comment is that a P or B will always overlap any other spaces that it's on.  
Herefore, it's possible that you don't see a GOLD or EXIT (or SPACE, but that's not that interesting fortunately) because you are (heh, ironic) or the bot is on it.  
Don't get paranoic at spawn however, as I won't make it so easy for you as to drop you on a gold tile right away!

```
___  ___             _                    _            
|  \/  |            | |                  (_)           
| .  . |  ___   ___ | |__    __ _  _ __   _   ___  ___ 
| |\/| | / _ \ / __|| '_ \  / _` || '_ \ | | / __|/ __|
| |  | ||  __/| (__ | | | || (_| || | | || || (__ \__ \
\_|  |_/ \___| \___||_| |_| \__,_||_| |_||_| \___||___/
```

This section covers a few useful things to know about the game.

### TURNS

The way the game works is in TURNS, which means that you and the bot each take turns doing a thing.  
This means that as you're carelessly PICKUP-ing gold, the BOT has another opportunity to move even closer to you!  
An additional possibly game-changing observation is that when you LOOK and see the BOT, it will in its next turn probably MOVE from that square to a new space: so try to anticipate its movements!   
By the way, even the COMMAND command takes up a turn, so better exercise those memory muscles!  
I'll go easy on you though, so when you type a command that doesn't exist you're permitted to try again as maaaaany times as you want without a single cost (except the precious few seconds of your time that you just wasted)!


***BOT MOVEMENT WATCH OUT THIS IS GAME-CHANGING TERRITORY AND I WOULD NOT RECOMMEND TO READ IT IF YOU WANT TO ENJOY THE GAME***  
Roughly put, the way the bot moves around is semi-random, and it uses the LOOK command whenever it wants to go somewhere it can't see.  
When the bot's look function sees you it will get to where you are now as quickly as possible, so make sure to escape!  
As I said earlier, the bot has the same limitation as you do, so it can only remember the last time it saw you and move towards that place.  
However, when it's there it will immediately LOOK again to see if you're still around...

See, I told you you shouldn't have read this, didn't I? I can see the regret in your face!

```
___  ___ _            
|  \/  |(_)           
| .  . | _  ___   ___ 
| |\/| || |/ __| / __|
| |  | || |\__ \| (__ 
\_|  |_/|_||___/ \___|
```

### CREATING YOUR OWN MAPS

Because maps are just simple txt-files, it's extremely simple to create your own ones.
I would recommend just using example_map.txt as a template:
* The file has to start with `name <name>`, where `<name>` is the map name you want the map to have;
* Then there's got to be a line `win <winGold>`, where `<winGold>` is the number of GOLD required to win;
* And then you can just put a map using the possible characters! 
  The map can be any size and as complicated as you want, just make sure it's a rectangle... and that it's possible to complete :)

So yeah, let your creative self have its way and make it as (un)fair and (un)intersting as you want!

And of course, if other people have created maps, it's as easy as pie to put those txt-files into your Project folder and play them.


### THE CODE

This game was written in Java (as should have been apparent from the commands I asked you to type in the beginning...), so if you're into that stuff I'd definitely recommend checking out the source code, as I've figured out some interesting methods to do stuff!  
However, even if you know nothing about Java: the code is very thoroughly commented so it might still be interesting to you to look at!

And, if you're even MORE interested, there's nothing stopping you from implementing your own features/players, is there? (＾ν＾)


### UNEXPECTED ERROR MESSAGES

In case of any unexpected error messages, please contact the author (i.e. me): contact details (more like "contact detail") are to be found below, or fix them by yourself if your a bug-fixing masochist like me ^°^

```
 _____                     _         _    _    _                    _         
/  ___|                   (_)       | |  | |  | |                  | |        
\ `--.  _ __    ___   ___  _   __ _ | |  | |_ | |__    __ _  _ __  | | __ ___ 
 `--. \| '_ \  / _ \ / __|| | / _` || |  | __|| '_ \  / _` || '_ \ | |/ // __|
/\__/ /| |_) ||  __/| (__ | || (_| || |  | |_ | | | || (_| || | | ||   < \__ \
\____/ | .__/  \___| \___||_| \__,_||_|   \__||_| |_| \__,_||_| |_||_|\_\|___/
       | |                                                                   
       |_|                          
```                                         
I want to issue special thanks to the person/website (?) called "vogella" for enabling the bot to kill YOU even MORE efficiently using state-of-the-art pathfinding technology!  
Check the source for the relevant java-classes at the link below:  
	https://github.com/vogellacompany/codeexamples-java/tree/master/de.vogella.algorithms.dijkstra/src/de/vogella/algorithms/dijkstra

Also thanks martinus @stackoverflow, for a nice'n'quick file line counter  
	https://stackoverflow.com/questions/453018/number-of-lines-in-a-file-in-java

```
 _____                _                _      _          __                                _    _               
/  __ \              | |              | |    (_)        / _|                              | |  (_)              
| /  \/  ___   _ __  | |_  __ _   ___ | |_    _  _ __  | |_  ___   _ __  _ __ ___    __ _ | |_  _   ___   _ __  
| |     / _ \ | '_ \ | __|/ _` | / __|| __|  | || '_ \ |  _|/ _ \ | '__|| '_ ` _ \  / _` || __|| | / _ \ | '_ \ 
| \__/\| (_) || | | || |_| (_| || (__ | |_   | || | | || | | (_) || |   | | | | | || (_| || |_ | || (_) || | | |
 \____/ \___/ |_| |_| \__|\__,_| \___| \__|  |_||_| |_||_|  \___/ |_|   |_| |_| |_| \__,_| \__||_| \___/ |_| |_|
                                                                                                                
```
Reach me (Jiri Swen) at this relatively obscure e-mail address:  
js3078@bath.ac.uk
