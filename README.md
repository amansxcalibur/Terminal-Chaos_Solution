# Terminal Chaos Admin Edition

To begin the challenge, the user must clone the repository into a folder of choice:

```bash
git@github.com:amansxcalibur/Terminal-Chaos.git
```
Or using https:
```bash
https://github.com/amansxcalibur/Terminal-Chaos.git
```

Now the user has to create a folder inside `amfoss-tasks/Task-02` named HandBook(optional). The user must create the folder using the command:

```bash
mkdir HandBook
```

The HandBook folder would be updated throughout the task.

## Part 1

```bash
cd Terminal-Chaos
```

Check the folder available for the user to move forward to using the command:
```bash
ls
```

The user would be able to move to four folders of which to continue the user must go to Arrakis-Dex followed by the Eolian Caves as instructed in the README. To do this the user must enter the following:

```bash
cd Arrakis-Dex
cd Eolian\ Caves/
```

Now the user must be confused since there are multiple `EntrancesX` folders. The folder having `parchment.txt` is the right one. Use the `tree` command to see the overall file structure.

```bash
tree
```

Now the user would be able to see that the path to `parchment.txt` is in the Entrance3. The user must enter the following command inside Eolian Caves:

```bash
cd Entrance3/01
```

Once we reach the `Entrance3/01`, using `cat parchment.txt` will give them the code for Part 1. If the users ran `medallion.py` before, it’s fine.

```bash
python3 medallion.py
cat parchment.txt
```

```
This is a record of the life of a young boy who aimed for the stars. Stuck in the cold and empty Arakkis, getting through the seal for any will be impossible. Unless they have access to the machine that rips open space-time itself. But getting ur hands on one should be a task of itself. The boy, even though put through the depths of the unknown, remained unfazed and continued his journey to the LIGHT REALM, where he found thXXXXXXXXXXX-


code: aHR0cHM6Ly9naXRo
```

This completes the first part of the Task. Store the code in a text file inside the `Handbook` directory and git push.

## Part 2

Now to begin the part 2 of the Task, the user must checkout to the Light Realm:

```bash
git checkout The-Light-Realm
```

Now it is recommended to go to the root directory of the entire project and enter it once again.

Now the aim of the user is to find all the files which have holy AND good herbs; for that, the user has to enter the command:

```bash
grep -rl 'holy.*good\|good.*holy'
```

The user could also find the files using the command `grep -rl "holy"` and manually finding the herbs which are good as well or vice versa. But if the user has used the above command without using any other command like xargs, they get plus points.

Now the user will get two herbs which are `Moonbloom.txt` and `Mistveil.txt`.

The user has to perform a cipher on this which is used to create a holy spell to defeat Kharnck the Bloodforged.

Cipher creation steps:
1. Append the names of the herbs => MoonbloomMistveil
2. Moving every letter to one set backwards in the alphabetical chart. (B=>A, b=>a, c=>b, and so on) => LnnmaknnlLhrsudhk
3. Removing vowels => LnnmknnlLhrsdhk

Now the cipher has to be submitted against the Khanrock for Defeating Khanrock.

Now we must find the Citadel where the fight awaits us:

```bash
cd /Terminal-Chaos/Arrakis-dex/Eolian Caves/Entrance3/01/01L/01/02/01/02/01/Citadel
python3 KharnokTheBloodForged.py
```

Successfully parry Kharnok three times and then enter the code for the holy spell `LnnmknnlLhrsdhk` to defeat him.

After defeating Kharnok, two files will be created, `LightBook.txt` and `Celestial Veil Amulet.txt`.

In these files lies the next two codes:

Inside the `LightBook.txt`:
```bash
cat LightBook.txt
```

```
Behold the Light Book!
A beacon of wisdom that illuminates the path of creation, peace, and enlightenment. The legends whisper of a hidden counterpart in the Dark Realm.
code:dWIuY29tL2FtYW5ze
```

Inside the `Celestial Veil Amulet.txt`:
```bash
cat Celestial\ Veil\ Amulet.txt
```
```
Forged in the celestial forges of Sigmaron, the Celestial Veil Amulet is a relic born of divine intervention to combat the malevolent forces that threaten the balance of existence. When worn, the Celestial Veil Amulet emanates a radiant glow, warding off malevolent influences and shielding the bearer from the corrupting touch of the Chaos.
code:CSigVmaroAn
```

Now save these both codes in the previously created text file inside the HandBook directory. This concludes Part 2.

## Part 3

Now the user has to go to the Dark Realm as adivised by the contents in the LightBook. Go to the `/Terminal-Chaos-User-Edition/Arrakis-dex/Eolian Caves/Entrance3/` repository from your current location and then enter the command:
```bash
git checkout The-Dark-Realm-I
```
Locate and go to the next location of DarkBook I from `Entrance3` directory using the following commands.
```
cd /Terminal-Chaos/Arrakis-dex/Eolian Caves/Entrance3/01/01D/01/narrow path/path/0D/02/01/Chamber
```
Run the python file `chest1.py` and enter the code of Celestial Amulet(CSigVmaroAn) to unlock the Chest and get the `DarkBookI.txt`.
```
python3 chest1.py
CSigVmaroAn
```
`DarkBookI.txt` will be created having the code: `GNhbGlidXIvVGVyb`

Now go to `/Terminal-Chaos/Arrakis-dex/Eolian Caves/Entrance3/01` and checkout to the Dark realm II:
```
git checkout The-Dark-Realm-II
```
Locate and go to the next location of the DarkBook from `Entrance3/01` directory using the following commands.
```
cd 01D/01/narrow\ path/path/0D/02/01/Chamber/
```
Run the python file `chest2.py` and enter the code of Celestial Amulet(CSigVmaroAn) to unlock the it and get the `DarkBookII.txt`.
```
python3 chest2.py
CSigVmaroAn
```
`DarkBookII.txt` will be created having the code: `WluYWwtQ2hhb3MtR29kU3VpdGU=`

Now the job of the user is to delete the chest files and merge both the branches (this step is optional, provide plus points if they do so).

`git merge The-Dark-Realm-I` or
```
git checkout The-Dark-Realm-I
git merge The-Dark-Realm-II
```

The user has to fix the conflicts in the file `SuspiciousPerson.txt`. The user may resolve the conflict in that file or delete the file to fix the merge conflict.

At the end the user would have two files `DarkBookI.txt` and `DarkBookII.txt` in the newly merged branch containing the codes:

```
GNhbGlidXIvVGVybWluYWwtQ2hhb3MtR29kU3VpdGU=
```

## Part 4

Now the user would have to append all the codes recieved from `parchment.txt`, `LightBook.txt`, `DarkBookI.txt` and `DarkBookII.txt` and convert it to normal string using a base64 decoder. They can use an online decoder or just do it in the terminal:
```bash
echo aHR0cHM6Ly9naXRodWIuY29tL2FtYW5zeGNhbGlidXIvVGVybWluYWwtQ2hhb3MtR29kU3VpdGU= | base64 --decode
```
Once decoded, a link to the GodSuite repository will be recieved:

https://github.com/amansxcalibur/Terminal-Chaos-GodSuite

## Part 5

Clone the repository mentioned above wherever you find comfortable.

```bash
git clone https://github.com/amansxcalibur/Terminal-Chaos-GodSuite
cd God-Suite/Open\ Book/
```

There are two ways to proceed from here. The aim is to find the version of `Scripture.txt` that contains the code. Either the user can look up versions of `Scripture.txt` containing the code using the `cat` command, or grep the word `portal` using the command:
```bash
grep -r "portal"
# or
# cat Scripture.txt
```
If the grep command returns nothing, it means the file does not have the word 'portal' in it. Therefore check the previous versions of the file via git using the command that follows.
```
git show HEAD~1:Open\ Book/Godsuite.txt
grep -r "portal"
# or
# cat Scripture.txt
```

Go through every commit and grep the word "portal" (or `cat` to find the code) to find `Scripture.txt` file version which has the location of the machine (the location will be revealed if you use grep) and help them escape. You can find the version which contains the word code through the command:
```
git show HEAD~3:Open\ Book/Godsuite.txt
grep -r "portal"
# or
# cat Scripture.txt
```
Using grep will show the line which reveals the location of the portal machine which is in `/Terminal-Chaos/Arrakis-dex/The Deep Desert E/9/4/Aridale/Voidgate Stronghold`.
The user can either convert the code using an online base64 converter or do it using the terminal
```bash
echo aHR0cHM6Ly9naXRodWIuY29tL2FuZ3JlemljaGF0dGVyYm94L1RvLXRoZS1zdGFycy1hbmQtcmVhbG1zLXVuc2Vlbg== | base64 -d
```
Or go to the `Terminal-Chaos` repo and go to the location of the portal machine specified in `Scripture.txt` of Godsuite and run the machine.
```bash
cd /Terminal-Chaos/Arrakis-dex/The\ Deep\ Desert\ E/9/4/Aridale/Voidgate\ Stronghold/
bash Voidgate.sh
#Enter the code below
aHR0cHM6Ly9naXRodWIuY29tL2FuZ3JlemljaGF0dGVyYm94L1RvLXRoZS1zdGFycy1hbmQtcmVhbG1zLXVuc2Vlbg==
```
 
Either way, the user should get the link to the victory repo:
https://github.com/angrezichatterbox/To-the-stars-and-realms-unseen

Clone the repository and run `victory.py` to get the victory message and complete Task 02.
Screenshot the victory message and paste it in your `amfoss-tasks/Task-02` repository.


