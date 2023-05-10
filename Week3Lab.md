# Week 3 Lab #

I used ChatGPT to look up these commands
-
##  **```grep``` searches for pattern(s) within a file or can search for a pattern within file names in a directory. It's useful when you want to search for a specific word or exact pattern, rather than a partial match.** ##



1. `grep -w` : searches for the whole word in the file. Useful if you want to search for words across a single or multiple files.

``` 
Input: grep -w "fax" 911report/*

Output: 
911report/chapter-1.txt:    He was, and is, right. But the conflict did not begin on 9/11. It had been publicly declared years earlier, most notably in a declaration faxed early in 1998 to an Arabic-language newspaper in London. Few Americans had noticed it. The fax had been sent from thousands of miles away by the followers of a Saudi exile gathered in one of the most remote and impoverished countries on earth.
911report/chapter-13.3.txt:                Sudanese regime notified him there by fax. See Tim Carney interview (Dec. 4, 2003);
911report/chapter-13.3.txt:                pp. 1575-1576). For Harun's fax, see government exhibit no. 300A-T, United States v.
911report/chapter-13.3.txt:            90. For the Atef fax, see government exhibit no. 1636-T, United States v. bin Laden.
911report/chapter-13.4.txt:                discovered among his possessions a fax copy of an advertisement for U.S. flight
```

***`grep -w` searched through all the 911reports `.txt` files and compared it to the word "fax". It returned the line with the word and the name of the file that has the word.*** 

```
Input: grep -w "Lee H. Hamilton" 911report/*

Output:
911report/chapter-13.3.txt:            107. For Congress's domestic orientation, see Lee H. Hamilton, How Congress Works and
911report/preface.txt:            Lee H. Hamilton, vice chair
```
***This is a more specific lookup the resulting output should have less files***

2. `grep -n ` : searches for the specific word in the file and returns the actual line contents and line number it appears. Helpful when you're  searching through a large file and want to quickly locate the exact line where a pattern appears.
``` 
Input: grep "n" "Payoffs" 911report/*

Output: 
911report/chapter-3.txt:870:                basic research, detailed and reflective. Payoffs might not be immediate. But when
```
***The number in between the two ```:``` ```:``` represents the line number the word appears in. Here, it appears on line 870.***
```
Input: grep -n "citizens" 911report/chapter-3.txt 

Output:
728:            The law requires the NSA to not deliberately collect data on U.S. citizens or on
1285:                vigorously to all terrorist attacks on our territory and against our citizens." The
1624:                as their reason their revocation of his citizenship.
1728:                Ladin's supporters might retaliate, perhaps taking U.S. citizens in Kandahar
```
***Since I specified which specific file and didn't use `*`, it didn't return the file name like the other example. It just display the line number and contents of the line the word appears in.***

3. ` grep -c `: returns the number of times the word appears. Helpful when you want to count the number of times a pattern appears in a file.

```
Input: grep -c "a" government/About_LSC/Comments_on_semiannual.txt 

Output: 
322
```
***This means that the word `a` appears in the file 322 times.***

```
Input: grep -c "asldkasfas" government/Alcohol_Problems/DraftRecom-PDF.txt 

Output: 
0
```
***This means that the word ```asldkasfas``` appears in the file 0 times.***

4. `grep -e`: allows you to search for multiple patterns or words. It is useful when you're searching for variations of a word or phrase.
 
``` 
Input:  grep -e "Ethics" -e "Ethical" plos/pmed.0020192.txt

Output: 
by her comment on our article. Nowhere in that article, “Ethics. Constructing Ethical
```
***Looked through the file for `Ethics` and `Ethical`. It is case-sensitive.***

```
Input: grep -e "Cox-2" -e "also" plos/pmed.0020197.txt

Output: 
cardiovascular disease. Caution may also extend to individuals predisposed to thrombosis by
        causative link to the COX-2 inhibitor. However, it also remains formally possible that this
        also interact with genetic and environmental factors that predispose to the risk of
```

***Each line has to contain at least one of the words you are comparing it to. Looked through the file for `Cox-2` and `also`.***
