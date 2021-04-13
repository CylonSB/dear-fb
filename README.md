# On the state and future of YOLOL

Dear Frozenbyte,  
with yolol you have given us a great tool to do a few awesome things. 
There already is a large community around, which is developing valuable scripts for all players, holds code-golf competitions and develops third-party tools for it.
Unfortunately it seems like yolol isn't getting as much love and attention from you, as it is getting from the playerbase.
There are quite a few issues with it and most of all, it's future seems to be a little uncertain. That really hinders any efforts taken by players to do great things with yolol.
Often people are asking themselves questions like: "Why should I invest any time and effort into something that might be gone (or heavily changed) at any time?" or "Is this weird behaviour I found a bug or intended? Should I adapt my 3rd-party tools accordingly, or will it be fixed eventually?"

That is why we, some members of the yolol-community, came together to ask you a few questions, to eventually shine some light onto the current state and the possible future of yolol.

We know that yolol is at the moment not really your top-priority. But to us yolol is a relatively important part of the game, which could really use a little bit more attention.

## Questions
Here are a few questions, that we really would like to have answered. Are there any plans to do the listed things? And most importantly what is
the time-schedule for these things? Please be as specific as you can.

1. Will yolol stay or will it eventually be replaced with something completely different (.e.g. Lua)
2. Will there be any changes to core-principles like the line- and character-limit or the tick-based nature?
3. Will there be changes to the syntax or semantics of the language? Things like replacing the "then...end" of if-statements with "{...}" for example,
 (which would probably make sense, given the hard character-limit.) Or having functions like abs, sin, cos require parenthesis?
4. Do you know about the bugs/issues listed below? Are you planning to fix them?
5. Would you be interested in some kind of online meetup between the community and some developers? We could try and shape the future of yolol together :)


## Bugs
This is a list of (some) known bugs in the ingame-parser. Some of these are really causing a lot of confusion and could probably be fixed easily.

1. The operator-precedence is a little broken. For example: ```+```/```-``` are evaluated after ```==```/```!=```
2. Variable-names can not contain any keywords. ```:life=1``` does not work, because ```if``` is a keyword and that breaks the parsing
3. ```i++``` and ```++i``` do exactly the same thing instead of doing Post-/Pre-Operations
4. The parser accepts some really weird stuff as correct. ```t++a++7++x++()++a--"yolol_is_great"++x++3===="test"``` simply parses as ```t="test"```
5. The parsing is context-dependent. Depending on if a variable has been used before or not, some lines are parsed differently.
6. When whitespace is and isn't required seems to be a little random

Not really "bugs" but still issues:  

7. The characters allowed inside variable-names are a bit weird. ```:_:``` is a valid variable-name.
8. There is a complete lack of feedback for syntax/runtime-errors ingame. Not getting told what is wrong with your code makes it REALLY hard for beginners
9. There is no language-specification (grammar, tokenization-rules, precedence etc.). That makes it impossible to find out if a certain behaviour is intended or a bug in the parser. Also, that makes it really hard to develop any 3rd party tools for yolol.

## With kind regards
- dbaumgarten#9279 (vscode-yolol, yodk)
- Martin#2468 aka Yolathothep (Cylon, YololEmulator, Referee)
- Dude112113#5906 (Yodine Tool)
- mrchip#4403
- Nyefari#1228 (Enthusiast)
- Max#0007 (DynaStar CEO)
- DirtyScoundrel#4096 (Cylon)
- Captain Wonders#4218 (DynaStar R&D / Shipyard Senior Staff)
- HeatProofTex#9789 (DynaStar Shipyard Manager)
- Short Man#2748 (DynaStar Shipyard Staff)
- Pasukaru#3669 (yolol.info)
- Azurethi#0789 (ISAN, Yazur)
- Zijkhal#0154
- Matrixmage#4830 (Cylon founder, Yoloxide, tool developer)
- rad dude broham#2970 (Cylon)
