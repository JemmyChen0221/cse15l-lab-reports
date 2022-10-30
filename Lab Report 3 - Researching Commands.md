# Lab Report 3 - Researching Commands
## 1 - Grep with `-i` command-line option

***Example1***
```
JemmyMashirodeMacBook-Pro:skill-demo1 jemmy$ cd technical/911report
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -i "existing" chapter-1.txt
    On the morning of 9/11, the existing protocol was unsuited in every respect for what was about to happen.
    The defense of U.S. airspace on 9/11 was not conducted in accord with preexisting training and protocols. It was improvised by civilians who had never handled a hijacked aircraft that attempted to disappear, and by a military unprepared for the transformation of commercial aircraft into weapons of mass destruction. As it turned out, the NEADS air defenders had nine minutes' notice on the first hijacked plane, no advance notice on the second, no advance notice on the third, and no advance notice on the fourth.
```
**Function?** 

The comman-line option `-i` is the case insensitive search, where it will search words no matter what their cases is. For example, in this case, I am searching for word `existing` in file `chapter-1.txt`. As you can see the word `existing` and `preexisting` have been found. It will also be able to seach words like `EXISTING` or `ExiSTing`.

**Useful?** 

It is useful because if we simply want to find where some word appeared but we do not care about the case, for exmaple, we want to see if some one mentioned a word in a transcript, we can simply use this way to see if there is any appearance. 




***Example2***
```
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -i "calmly" chapter-1.txt
    About five minutes after the hijacking began, Betty Ong contacted the American Airlines Southeastern Reservations Office in Cary, North Carolina, via an AT&T airphone to report an emergency aboard the flight. This was the first of several occasions on 9/11 when flight attendants took action outside the scope of their training, which emphasized that in a hijacking, they were to communicate with the cockpit crew. The emergency call lasted approximately 25 minutes, as Ong calmly and professionally relayed information about events taking place aboard the airplane to authorities on the ground.
    Sweeney calmly reported on her line that the plane had been hijacked; a man in first class had his throat slashed; two flight attendants had been stabbed-one was seriously hurt and was on oxygen while the other's wounds seemed minor; a doctor had been requested; the flight attendants were unable to contact the cockpit; and there was a bomb in the cockpit. Sweeney told Woodward that she and Ong were trying to relay as much information as they could to people on the ground.
```
**Function?** 

The use of this command works same as above. `grep -i "calmly" chapter-1.txt` is tryign to find the word `calmly` in the file chapter-1.txt. Of couse, this is again case insensitive, so whatever case will be identified.  

**Useful?**

It is useful since we will be able to knwo where to look into the text about the word we are interested in. This is also useful when doing research since we will be able know which paragraph to focus when wanting to know certain stuff.





***Example3***

```
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -i "Presumably" chapter-1.txt
    At about 8:55, the controller in charge notified a New York Center manager that she believed United 175 had also been hijacked. The manager tried to notify the regional managers and was told that they were discussing a hijacked aircraft (presumably American 11) and refused to be disturbed. At 8:58, the New York Center controller searching for United 175 told another New York controller "we might have a hijack over here, two of them."
    At 10:02, the communicators in the shelter began receiving reports from the Secret Service of an inbound aircraft-presumably hijacked-heading toward Washington. That aircraft was United 93. The Secret Service was getting this information directly from the FAA. The FAA may have been tracking the progress of United 93 on a display that showed its projected path to Washington, not its actual radar return. Thus, the Secret Service was relying on projections and was not aware the plane was already down in Pennsylvania.
    Second, NEADS did not have accurate information on the location of United 93. Presumably FAA would have provided such information, but we do not know how long that would have taken, nor how long it would have taken NEADS to locate the target.

```
**Function?**
The use of this command again works same as above. `grep -i "Presumably" chapter-1.txt`. It is finding any occurence of the word `Presumably` in the file`chater-1.txt`. You can see that finally in this case, we can see both `presumably American 11` and `resumably FAA would have provided...` is being shown, and yet that have different case. Thus, it shows that the command-line option -i shows the case insensitive search result. 

**Useful?**
It is useful since when we are trying to see if a word occurs in a passage, it is often complicated to search it twice using the word `presumably` and `Presumably`. Which is pretty time comsuimg. Thus, suing this way of searching, we see that it takes a lot less effore to do all the search. 

---

## 2- Grep with `-c` command-line option
***Example1***

```
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -c "existing" chapter-1.txt
2
```

**Function?**
This workds similar to command-line option `-i`, but it actually did the last step a littel differently. In `-i` it is finding the word and print them out. However, in this case, `-c` is doing the process of finding that occurecne and count the occurence. And in the end, return the number of occurence of certain pattern. 

**Useful?**
It is useful since we are able to knwo the number of occurence in someword in a file, instead of us to count them out one by one. It really helps save time and let us to process large data easier. 





***Example2***
```
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -c "President" chapter-1.txt
41

JemmyMashirodeMacBook-Pro:911report jemmy$ grep -c "president" chapter-1.txt
6
```
**Function?**
This work again similar to above, but one thing to note is that, in this case, `-c` is not case insensitive. As you can tell from above, the word `President` and `president` shows different result. 

**Useful?**
This is useful to know that we can distinguish the two cases. If we want to know all the occurence of something, we can simply just add them up, by doing `grep -c "President" chapter-1.txt` + `grep -c "president" chapter-1.txt`. This is useful to when doing large data search on some research. 





***Example3***
```
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -c "aircraft" chapter-1.txt
121
```
**Function?**
This work again similart to above, and this process really quick, even there are 121 occurence of the patter. It searches the word `aircraft` in the file, and it says there are 121 occurence, note that this only refers to `aircraft` with all lower case. 

**Useful?**
This is useful since we know it can process large datasert in less than a seconds, so we can be able to run a lot of file, and find the total occurence of some certain pattern. This is useful when doign a report on soething, say like a transcript, we can easily know how many times a person mentione a word. 


---

## 3 - Grep with `-l` command-line option

***Example1***

```
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -l "existing" *
chapter-1.txt
chapter-10.txt
chapter-11.txt
chapter-12.txt
chapter-13.1.txt
chapter-13.4.txt
chapter-13.5.txt
chapter-2.txt
chapter-3.txt
chapter-6.txt
chapter-8.txt
chapter-9.txt
```
**Function?**
This is a really good function in my opioin. The command-line option `-l` is able to find the word from a directory, and display all the files that contain that pattern. In this case, we are find the word `existing` in all file under directory `911report`.

**Useful?**
It is extremly useful since we are able to distinguish what files should we look into if we are especially interested in something. Say we have a large dataset, and we want to distinguish all the interested file, we can use this way to dinsinguish them.





***Example2***
```
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -l "aircraft" *
chapter-1.txt
chapter-10.txt
chapter-11.txt
chapter-12.txt
chapter-13.2.txt
chapter-13.3.txt
chapter-13.4.txt
chapter-13.5.txt
chapter-2.txt
chapter-3.txt
chapter-5.txt
chapter-6.txt
chapter-7.txt
chapter-8.txt
chapter-9.txt
```
**Function?**
This again did a similar thing as above, we see that it is trying to find which file in the directory `911report` has the occurence of `aircraft`. And it prints out many file that contains the word`aircraft`.

**Useful?**
It is useful since we see that we are able use one word that we are interested to classify all the files into the one we are interested. Then we can start looking at them, and it will save a lot of time. 





***Example3***
```
JemmyMashirodeMacBook-Pro:911report jemmy$ grep -l "crash" *
chapter-1.txt
chapter-10.txt
chapter-11.txt
chapter-12.txt
chapter-13.2.txt
chapter-13.3.txt
chapter-13.4.txt
chapter-13.5.txt
chapter-5.txt
chapter-7.txt
chapter-8.txt
chapter-9.txt

JemmyMashirodeMacBook-Pro:911report jemmy$ grep -l "Crash" *
chapter-13.2.txt
```
**Function?**
It again work similar as above, it return all the file in `911report` that has the word crash in it. One thing to note that, I did a simialr thing as the one I did on `-c`. The command-line option `-l` is not case insensitive. Since we can tell that the word `Crash` and `crash` shows two different results.

**Useful?**
It is useful to know that it is case sensitive, since if we are tryind to find certain words, but if it not case sensitive, it might give us other result. For example, we want to find the word `CSE`, but if it is not case sensive, the word `cse` might shows, and we are not really interested in that. 

