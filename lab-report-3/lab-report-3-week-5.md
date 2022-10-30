# Lab Report 3

## Command Line Option #1 : `grep -c` 

- The `grep -c` command can allow the user to easily search for a certain keyword or phrase in multiple files simultaneously and return the number of lines that they are found in.

### Example 1
```
[cs15lfa22if@ieng6-202]:~:222$ ls                                                                                       
Lab1  Lab2  docsearch  path-examples  perl5  skill-demo1                                                                [cs15lfa22if@ieng6-202]:~:223$ cd docsearch                                                                             [cs15lfa22if@ieng6-202]:docsearch:224$ cd technical                                                                     [cs15lfa22if@ieng6-202]:technical:225$ cd plos                                                                          [cs15lfa22if@ieng6-202]:plos:226$ grep -c "medical" journal.pbio.*                                                      
journal.pbio.0020001.txt:1                                                                                              
journal.pbio.0020010.txt:0                                                                                              
journal.pbio.0020012.txt:0                                                                                              
journal.pbio.0020013.txt:0                                                                                              
journal.pbio.0020019.txt:0                                                                                              
journal.pbio.0020028.txt:0                                                                                              
journal.pbio.0020035.txt:0                                                                                              
journal.pbio.0020040.txt:0                                                                                              
journal.pbio.0020042.txt:0                                                                                             
journal.pbio.0020043.txt:0                                                                                              
journal.pbio.0020046.txt:0                                                                                              
journal.pbio.0020047.txt:1                                                                                              
journal.pbio.0020052.txt:0                                                                                              
journal.pbio.0020053.txt:1                                                                                              
journal.pbio.0020054.txt:0                                                                                             
journal.pbio.0020063.txt:19                                                                                            
journal.pbio.0020064.txt:0                                                                                              
journal.pbio.0020067.txt:0                                                                                              
journal.pbio.0020068.txt:0                                                                                              
journal.pbio.0020071.txt:0                                                                                              
journal.pbio.0020073.txt:0                                                                                              
journal.pbio.0020100.txt:0                                                                                              
journal.pbio.0020101.txt:0                                                                                              
journal.pbio.0020105.txt:0                                                                                              
journal.pbio.0020112.txt:0                                                                                              
journal.pbio.0020113.txt:0                                                                                              
journal.pbio.0020116.txt:7                                                                                              
journal.pbio.0020121.txt:0                                                                                              
journal.pbio.0020125.txt:0                                                                                              
journal.pbio.0020127.txt:0                                                                                              
journal.pbio.0020133.txt:0                                                                                              
journal.pbio.0020140.txt:0                                                                                              
journal.pbio.0020145.txt:0                                                                                              
journal.pbio.0020146.txt:0                                                                                              
journal.pbio.0020147.txt:0                                                                                              
journal.pbio.0020148.txt:0                                                                                              
journal.pbio.0020150.txt:1                                                                                              
journal.pbio.0020156.txt:1                                                                                              
journal.pbio.0020161.txt:0                                                                                              
journal.pbio.0020164.txt:0                                                                                              
journal.pbio.0020169.txt:0                                                                                              
journal.pbio.0020172.txt:0                                                                                              
journal.pbio.0020183.txt:0                                                                                              
journal.pbio.0020187.txt:3                                                                                              
journal.pbio.0020190.txt:0                                                                                              
journal.pbio.0020206.txt:0                                                                                              
journal.pbio.0020213.txt:0                                                                                              
journal.pbio.0020214.txt:0                                                                                              
journal.pbio.0020215.txt:0                                                                                              
journal.pbio.0020216.txt:0                                                                                              
journal.pbio.0020223.txt:0                                                                                              
journal.pbio.0020224.txt:0                                                                                              
journal.pbio.0020228.txt:4                                                                                              
journal.pbio.0020232.txt:0                                                                                              
journal.pbio.0020241.txt:0                                                                                              
journal.pbio.0020262.txt:0                                                                                             
journal.pbio.0020263.txt:0                                                                                              
journal.pbio.0020267.txt:0                                                                                              
journal.pbio.0020272.txt:0                                                                                              
journal.pbio.0020276.txt:1                                                                                              
journal.pbio.0020297.txt:0                                                                                              
journal.pbio.0020302.txt:0                                                                                              
journal.pbio.0020306.txt:0                                                                                              
journal.pbio.0020307.txt:0                                                                                              
journal.pbio.0020310.txt:0                                                                                              
journal.pbio.0020311.txt:0                                                                                              
journal.pbio.0020337.txt:0                                                                                              
journal.pbio.0020346.txt:0                                                                                              
journal.pbio.0020347.txt:0                                                                                              
journal.pbio.0020348.txt:0                                                                                              
journal.pbio.0020350.txt:0                                                                                              
journal.pbio.0020353.txt:4                                                                                              
journal.pbio.0020354.txt:0                                                                                              
journal.pbio.0020394.txt:0                                                                                              
journal.pbio.0020400.txt:0                                                                                              
journal.pbio.0020401.txt:0                                                                                              
journal.pbio.0020404.txt:0                                                                                              
journal.pbio.0020406.txt:0                                                                                             
journal.pbio.0020419.txt:0                                                                                              
journal.pbio.0020420.txt:0                                                                                              
journal.pbio.0020430.txt:0                                                                                              
journal.pbio.0020431.txt:0                                                                                              
journal.pbio.0020439.txt:0                                                                                              
journal.pbio.0020440.txt:1                                                                                              
journal.pbio.0030021.txt:0                                                                                              
journal.pbio.0030024.txt:0                                                                                              
journal.pbio.0030032.txt:0                                                                                              
journal.pbio.0030050.txt:0                                                                                              
journal.pbio.0030051.txt:0                                                                                              
journal.pbio.0030056.txt:0                                                                                             
journal.pbio.0030062.txt:0                                                                                              
journal.pbio.0030065.txt:0                                                                                              
journal.pbio.0030076.txt:0                                                                                              
journal.pbio.0030094.txt:0                                                                                              
journal.pbio.0030097.txt:2                                                                                              
journal.pbio.0030102.txt:0                                                                                              
journal.pbio.0030105.txt:0                                                                                              
journal.pbio.0030127.txt:0                                                                                              
journal.pbio.0030129.txt:0                                                                                              
journal.pbio.0030131.txt:0                                                                                              
journal.pbio.0030136.txt:0                                                                                              
journal.pbio.0030137.txt:0
```                                                      
- In this example, I wanted to determine specifically which `journal.pbio` files were oriented towards the medical field in the `/plos` directory. Using the `-c` command, I was able to determine that `journal.pbio.0020063.txt` could be the most medically oriented because `medical` was used the most in it.

### Example 2
```
[cs15lfa22if@ieng6-202]:technical:229$ cd 911report                                                                     [cs15lfa22if@ieng6-202]:911report:230$ grep -c "World Trade Center" chapter-9.txt                                       16                
```
- In this example, I used the `grep -c` command to determine how many times the World Trade Center is mentioned in the text file. This could be useful when trying to determine the how many times a word is used in a text.

### Example 3
```
[cs15lfa22if@ieng6-202]:911report:254$ grep -c "PREFACE" *.txt                                                          chapter-1.txt:0                                                                                                         chapter-10.txt:0                                                                                                        chapter-11.txt:0                                                                                                        chapter-12.txt:0                                                                                                        chapter-13.1.txt:0                                                                                                      chapter-13.2.txt:0                                                                                                      chapter-13.3.txt:0                                                                                                      chapter-13.4.txt:0                                                                                                      chapter-13.5.txt:0                                                                                                      chapter-2.txt:0                                                                                                         chapter-3.txt:0                                                                                                         chapter-5.txt:0                                                                                                         chapter-6.txt:0                                                                                                         chapter-7.txt:0                                                                                                         chapter-8.txt:0                                                                                                         chapter-9.txt:0                                                                                                         preface.txt:1                
```
- In this example, I used the `PREFACE` keyword in order to find the text file with the preface for the narrative. This would be very useful in the case someone wanted to find a certain chapter or section within multiple text files, but it was not explicitly stated within the file names.

## Command Line Option #2: `grep -w`



```
[cs15lfa22if@ieng6-202]:911report:257$ grep -w "terrorism" chapter-12.txt                                                               our nation in this new era. The national debate continues. Countering terrorism has                                     terrorism. Between fiscal year 2001, the last budget adopted before 9/11, and the                                       societies than by the territorial boundaries between them. From terrorism to global                                     has taught us that terrorism against American interests "over there" should be                                          regarded just as we regard terrorism against America "over here." In this same                                          sense, the American homeland is the planet. But the enemy is not just "terrorism,"                                      is more specific. It is the threat posed by Islamist terrorism-especially the al                                        terrorism.                                                                                                              transnational danger is Islamist terrorism. What is needed is a broad                                                   prevent the continued growth of Islamist terrorism; and                                                             Certainly the strategy should include offensive operations to counter terrorism.                                            terrorism? The goals seem unlimited: Defeat terrorism anywhere in the world. But                                        terrorism. Within Pakistan's borders are 150 million Muslims, scores of al Qaeda                                        On terrorism, Pakistan helped nurture theTaliban. The Pakistani army and                                                    international crime and terrorism. The United States and the international                                          cooperation against terrorism improved to some extent after the September 11                                        As in Pakistan, Yemen, and other countries, attitudes changed when the terrorism came                                           terrorism."                                                                                                     Cooperation with Saudi Arabia against Islamist terrorism is very much in the U.S.                                           terrorism, Defense Secretary Donald Rumsfeld asked his advisers:"Are we capturing,                                      conflict against Islamist terrorism.                                                                                    right thing in its fight against terrorism; few people saw popular support for al                                       safer if worldwide Islamist terrorism grows stronger.                                                                   Islamist terrorism.                                                                                                     societies break down, when countries fragment, the breeding grounds for terrorism                                       Recommendation: A comprehensive U.S. strategy to counter terrorism                                                          developing a comprehensive coalition strategy against Islamist terrorism. There                                     struggle against Islamist terrorism is not internal, those provisions do not                                        The coalition strategies we have discussed to combat Islamist terrorism should                                              security in an age of terrorism is to prevent the very few people who may pose                                          terrorism-inevitably shaped al Qaeda's planning and opportunities. Because they were                                        tactics, such as use of insiders, suicide terrorism, or standoff attack. Each 
```
