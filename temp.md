* The command I will be exploring is `grep`

1) `grep -w`
* The source where I found this interesting command line option is: [Geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
```
[cs15lwi23aby@ieng6-203]:skill-demo1-data:382$ grep -w "Lucayans" written_2/*/*/*
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
* This command listed the surrounding text of the files in `written_2` that contained the exact word "Lucayans"
* This command is useful if you are searching for a word that can appear as a substring in a longer word
```
[cs15lwi23aby@ieng6-203]:skill-demo1-data:391$ grep -w "small Chinatown" written_2/*/*/*
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt:Central Havana is a ramshackle residential and commercial area. The city’s main shopping street, Calle San Rafael, traverses it from the Parque Central westward. This might be Havana at its least guarded. While having a fascinating stroll here, you can stop to have your nails painted, or get a shave and a haircut, all right on the pavement. One of the country’s new private markets has overrun Havana’s small Chinatown, at Calles Zanja and Rayo. Amazingly, even downtrodden Central Havana is being transformed by the presence of glittering dollar stores.
```
* This command listed the surrounding text of the files in `written_2` that contained the exact word "small Chinatown"
* This command is useful if you are searching for a word that can appear as a substring in a longer word
* If you had used the command `grep -w "small China"` this result would not have showed up
* If you had used the command `grep "small China"` this result would have showed up

2) `grep -l`
* The source where I found this interesting command line option is: [Geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
```
[cs15lwi23aby@ieng6-203]:skill-demo1-data:380$ grep -l  "Lucayans" written_2/*/*/*
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
written_2/travel_guides/berlitz2/Bahamas-History.txt
```
* This command listed the file name of the files in `written_2` that contained the word "Lucayans"
* This command is useful if you want to know if a word appears in a file
```
[cs15lwi23aby@ieng6-203]:skill-demo1-data:381$ grep -l "Jesus" written_2/*/*/*
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
written_2/travel_guides/berlitz1/HistoryIsrael.txt
written_2/travel_guides/berlitz1/HistoryJapan.txt
written_2/travel_guides/berlitz1/HistoryJerusalem.txt
written_2/travel_guides/berlitz1/IntroIsrael.txt
written_2/travel_guides/berlitz1/IntroJerusalem.txt
written_2/travel_guides/berlitz1/WhereToDublin.txt
written_2/travel_guides/berlitz1/WhereToEgypt.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz1/WhereToIndia.txt
written_2/travel_guides/berlitz1/WhereToIsrael.txt
written_2/travel_guides/berlitz1/WhereToIstanbul.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
written_2/travel_guides/berlitz1/WhereToJapan.txt
written_2/travel_guides/berlitz1/WhereToJerusalem.txt
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
written_2/travel_guides/berlitz1/WhereToMadrid.txt
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt
written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
```
* This command listed the file name of the files in `written_2` that contained the word "Jesus"
* This command is useful if you want to know if a word appears in a file
* As you can see, this is especially helpful if the word appears in many files, because the terminal won't be filled with text unlike a normal `grep` command

3) `grep -n`
* The source where I found this interesting command line option is: [Geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
```
[cs15lwi23aby@ieng6-203]:skill-demo1-data:394$ grep -n "Lucayans" written_2/*/*/*
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
written_2/travel_guides/berlitz2/Bahamas-History.txt:6:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:7:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
* This command listed the surrounding text and line number of the word of the files in `written_2` that contained the word "Lucayans"
* This command is useful if you want to know where a word appears in a file
```
[cs15lwi23aby@ieng6-203]:skill-demo1-data:395$ grep -n "colonialism" written_2/*/*/*
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
written_2/travel_guides/berlitz1/WhereToEgypt.txt:30:        Station, designed in the heyday of colonialism and fronted by a
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:528:        The echoes of colonialism are clearly evident in the
written_2/travel_guides/berlitz2/Bali-History.txt:28:The period between 1959 and 1965 was a surreal time of government by means of slogans and Orwellian acronyms. Sukarno attempted to control the competing nationalist, religious, and communist groups; NASAKOM was the word he used to represent their supposed common interests. As if that wasn’t enough, processions paraded with placards emblazoned with MANIPOL (Sukarno’s political manifesto) and DEKON (his economic declaration) written on them, and there were others which condemned NEKOLIM (neo-colonialism and imperialism). In the meantime, the Indonesian economy collapsed and hyper-inflation destroyed the currency.
```
* This command listed the surrounding text and line number of the word of the files in `written_2` that contained the word "colonialism"
* This command is useful if you want to know where a word appears in a file
* If you want to look at the file, you will have a better idea of where the word is

4) `grep -C n`
* The source where I found this interesting command line option is: [Geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
```
[cs15lwi23aby@ieng6-203]:skill-demo1-data:396$ grep -C 1 "Lucayans" written_2/*/*/*
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
written_2/travel_guides/berlitz2/Bahamas-History.txt-A Brief History
written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
written_2/travel_guides/berlitz2/Bahamas-History.txt-English sea captains also came to know the beautiful but deserted Bahamian islands during the 17th century. England’s first formal move was on 30 October 1629, when Charles I granted the Bahamas and a chunk of the American south to his Attorney General, Sir Robert Health. But nothing came of that, nor of a rival French move in 1633 when Cardinal Richelieu, the 17th-century French statesman, tried claiming the islands for France. 
```
* n is the number of lines before and after the word you are searching for
* if you try to put n as a negative number or decimal, an exception is thrown
* This command listed 1 line before and after of the surrounding text of the files in `written_2` that contained the word "Lucayans" and the name of the chapter
* This command is useful if you want to see the word you are searching for in context
```
[cs15lwi23aby@ieng6-203]:skill-demo1-data:399$ grep -C 1 "programming" written_2/*/*/*
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt-Universal Studios Florida
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt:This theme park where you can “ride the movies” is a huge complex of futuristic and computerized rides based on movie themes. Come face to face with Jaws or ride out a Twister. It feels as if you’re really part of the action as your carriage jolts around corners and flames lick close to your seat (all carefully choreographed for utmost safety). Enjoy the fun of the Nickelodeon Studios, where kids programming takes center stage. There are parades and stunt spectaculars and plenty of places to eat. Universal Studios is located off I-4; take exits 29 or 30B.
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt-Orlando Flextickets offer a combination ticket for Sea World, Universal Studios, and the Wet-and-Wild water complex in Orlando; for details call 800-224-3838 of consult the Universal Studios’ website, <www.usf.com>.
```
* n is the number of lines before and after the word you are searching for
* if you try to put n as a negative number or decimal, an exception is thrown
* This command listed 1 line before and after of the surrounding text of the files in `written_2` that contained the word "programming" and the name of the chapter
* This command is useful if you want to see the word you are searching for in context

