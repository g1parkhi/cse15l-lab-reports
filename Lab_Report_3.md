# Lab Report 3

## Command

> I will research the **grep** command.

> I will demonstrate using options on files from ./written_2

## Option 1 : **-h**
> 2 examples of using **-h** on files from ./written_2

Example 1)
```
# Command
grep -h "Aston" ./written_2/travel_guides/berlitz1/*    

# Output
Aston Waikiki Sunset $$$ 229 Paoakalani Avenue, Honolulu, HI
<www.aston-hotels.com>. One of Aston’s many condominium resort
```
In this example, I used '-h' option for 'grep' command.
The option forces the vsCode to never print filename headers (i.e., filenames) with output lines.
As shown in the output, although the program located the lines where string "Aston" is in,
it only prints out the lines and doesn't display the filenames (which would be HandRHawaii.txt if shown).

Example 2)
```
# Command
grep -h "Akko Beach" ./written_2/travel_guides/berlitz1/*  

# Output
Palm Beach Hotel and Country Club ❁❁-❁❁❁ Akko Beach; Tel.
```
In this example, I used '-h' option again for 'grep' command.
The option forces the vsCode to never print filename headers (i.e., filenames) with output lines.
As shown in the output, although the program located the lines where string "Akko Beach" is in,
it only prints out the lines and doesn't display the filenames (which would be HandRIsrael.txt if shown).

Usage)
The usage of option '-h' can be better explained by comparison to '-H' option.
'-H' option forces the program to always print filename headers (i.e. filenames) with output lines.
If I replaced the the option to '-H' in example 2, the following result comes out.
```
# Command
grep -H "Akko Beach" ./written_2/travel_guides/berlitz1/*  

# Output
./written_2/travel_guides/berlitz1/HandRIsrael.txt:        Palm Beach Hotel and Country Club ❁❁-❁❁❁ Akko Beach; Tel.
```
As shown, the file name is printed out.
The reason '-h' command is useful is because it allows the user to check only the output lines.
If the user already knows the filename or doesn't care about it and wants only the output lines, '-h' option
get rids of filename headers and dramatically increases the readability.

Reference: 'man grep' command, ChatGPT


## Option 2 : **-c**
> 2 examples of using **-c** on files from ./written_2

Example 1)
```
# Command
grep -c "Norman" ./written_2/travel_guides/berlitz1/*

# Output
./written_2/travel_guides/berlitz1/HandRHawaii.txt:0
./written_2/travel_guides/berlitz1/HandRHongKong.txt:0
./written_2/travel_guides/berlitz1/HandRIbiza.txt:0
./written_2/travel_guides/berlitz1/HandRIsrael.txt:0
./written_2/travel_guides/berlitz1/HandRIstanbul.txt:0
./written_2/travel_guides/berlitz1/HandRJamaica.txt:8
./written_2/travel_guides/berlitz1/HandRJerusalem.txt:0
./written_2/travel_guides/berlitz1/HandRLakeDistrict.txt:0
./written_2/travel_guides/berlitz1/HandRLasVegas.txt:0
./written_2/travel_guides/berlitz1/HandRLisbon.txt:0
./written_2/travel_guides/berlitz1/HandRLosAngeles.txt:0
./written_2/travel_guides/berlitz1/HandRMadeira.txt:0
./written_2/travel_guides/berlitz1/HandRMadrid.txt:0
./written_2/travel_guides/berlitz1/HandRMallorca.txt:0
./written_2/travel_guides/berlitz1/HistoryDublin.txt:8
./written_2/travel_guides/berlitz1/HistoryEdinburgh.txt:0
./written_2/travel_guides/berlitz1/HistoryEgypt.txt:0
./written_2/travel_guides/berlitz1/HistoryFWI.txt:1
./written_2/travel_guides/berlitz1/HistoryFrance.txt:5
./written_2/travel_guides/berlitz1/HistoryGreek.txt:0
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:0
./written_2/travel_guides/berlitz1/HistoryHongKong.txt:0
./written_2/travel_guides/berlitz1/HistoryIbiza.txt:0
./written_2/travel_guides/berlitz1/HistoryIndia.txt:0
./written_2/travel_guides/berlitz1/HistoryIsrael.txt:0
./written_2/travel_guides/berlitz1/HistoryIstanbul.txt:0
./written_2/travel_guides/berlitz1/HistoryItaly.txt:4
./written_2/travel_guides/berlitz1/HistoryJamaica.txt:2
./written_2/travel_guides/berlitz1/HistoryJapan.txt:0
./written_2/travel_guides/berlitz1/HistoryJerusalem.txt:0
./written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt:3
./written_2/travel_guides/berlitz1/HistoryLasVegas.txt:0
./written_2/travel_guides/berlitz1/HistoryMadeira.txt:0
./written_2/travel_guides/berlitz1/HistoryMadrid.txt:0
./written_2/travel_guides/berlitz1/HistoryMalaysia.txt:0
./written_2/travel_guides/berlitz1/HistoryMallorca.txt:0
./written_2/travel_guides/berlitz1/IntroDublin.txt:0
./written_2/travel_guides/berlitz1/IntroEdinburgh.txt:0
./written_2/travel_guides/berlitz1/IntroEgypt.txt:0
./written_2/travel_guides/berlitz1/IntroFWI.txt:0
./written_2/travel_guides/berlitz1/IntroFrance.txt:3
./written_2/travel_guides/berlitz1/IntroGreek.txt:0
./written_2/travel_guides/berlitz1/IntroHongKong.txt:0
./written_2/travel_guides/berlitz1/IntroIbiza.txt:0
./written_2/travel_guides/berlitz1/IntroIndia.txt:0
./written_2/travel_guides/berlitz1/IntroIsrael.txt:0
./written_2/travel_guides/berlitz1/IntroIstanbul.txt:0
./written_2/travel_guides/berlitz1/IntroItaly.txt:1
./written_2/travel_guides/berlitz1/IntroJamaica.txt:0
./written_2/travel_guides/berlitz1/IntroJapan.txt:0
./written_2/travel_guides/berlitz1/IntroJerusalem.txt:0
./written_2/travel_guides/berlitz1/IntroLakeDistrict.txt:0
./written_2/travel_guides/berlitz1/IntroLasVegas.txt:0
./written_2/travel_guides/berlitz1/IntroLosAngeles.txt:0
./written_2/travel_guides/berlitz1/IntroMadeira.txt:0
./written_2/travel_guides/berlitz1/IntroMadrid.txt:0
./written_2/travel_guides/berlitz1/IntroMalaysia.txt:0
./written_2/travel_guides/berlitz1/IntroMallorca.txt:0
./written_2/travel_guides/berlitz1/JungleMalaysia.txt:0
./written_2/travel_guides/berlitz1/WhatToDublin.txt:0
./written_2/travel_guides/berlitz1/WhatToEdinburgh.txt:0
./written_2/travel_guides/berlitz1/WhatToEgypt.txt:0
./written_2/travel_guides/berlitz1/WhatToFWI.txt:0
./written_2/travel_guides/berlitz1/WhatToFrance.txt:0
./written_2/travel_guides/berlitz1/WhatToGreek.txt:0
./written_2/travel_guides/berlitz1/WhatToHawaii.txt:0
./written_2/travel_guides/berlitz1/WhatToHongKong.txt:0
./written_2/travel_guides/berlitz1/WhatToIbiza.txt:0
./written_2/travel_guides/berlitz1/WhatToIndia.txt:0
./written_2/travel_guides/berlitz1/WhatToIsrael.txt:0
./written_2/travel_guides/berlitz1/WhatToIstanbul.txt:0
./written_2/travel_guides/berlitz1/WhatToItaly.txt:0
./written_2/travel_guides/berlitz1/WhatToJamaica.txt:2
./written_2/travel_guides/berlitz1/WhatToJapan.txt:0
./written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:0
./written_2/travel_guides/berlitz1/WhatToLasVegas.txt:0
./written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:0
./written_2/travel_guides/berlitz1/WhatToMadeira.txt:0
./written_2/travel_guides/berlitz1/WhatToMalaysia.txt:0
./written_2/travel_guides/berlitz1/WhatToMallorca.txt:0
./written_2/travel_guides/berlitz1/WhereToDublin.txt:4
./written_2/travel_guides/berlitz1/WhereToEdinburgh.txt:0
./written_2/travel_guides/berlitz1/WhereToEgypt.txt:0
./written_2/travel_guides/berlitz1/WhereToFWI.txt:2
./written_2/travel_guides/berlitz1/WhereToFrance.txt:24
./written_2/travel_guides/berlitz1/WhereToGreek.txt:0
./written_2/travel_guides/berlitz1/WhereToHawaii.txt:0
./written_2/travel_guides/berlitz1/WhereToHongKong.txt:1
./written_2/travel_guides/berlitz1/WhereToIbiza.txt:0
./written_2/travel_guides/berlitz1/WhereToIndia.txt:0
./written_2/travel_guides/berlitz1/WhereToIsrael.txt:0
./written_2/travel_guides/berlitz1/WhereToIstanbul.txt:0
./written_2/travel_guides/berlitz1/WhereToItaly.txt:11
./written_2/travel_guides/berlitz1/WhereToJapan.txt:0
./written_2/travel_guides/berlitz1/WhereToJerusalem.txt:0
./written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt:3
./written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:0
./written_2/travel_guides/berlitz1/WhereToMadeira.txt:0
./written_2/travel_guides/berlitz1/WhereToMadrid.txt:0
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt:4
./written_2/travel_guides/berlitz1/WhereToMallorca.txt:0
```
In this example, I used '-c' option for 'grep' command.
The option counts the number of occurences of the string, "Norman" and prints it out.
As shown in the output, string "Norman" shows up in files such as WhereToFWI.txt. It also denotes how many times
the string appears in the file. For instance, "Norman" appears 24 times in WhereToFrance.txt.

Example 2)
```
# Command
grep -c "US" ./written_2/travel_guides/berlitz1/*    

# Output
./written_2/travel_guides/berlitz1/HandRHawaii.txt:0
./written_2/travel_guides/berlitz1/HandRHongKong.txt:0
./written_2/travel_guides/berlitz1/HandRIbiza.txt:0
./written_2/travel_guides/berlitz1/HandRIsrael.txt:0
./written_2/travel_guides/berlitz1/HandRIstanbul.txt:0
./written_2/travel_guides/berlitz1/HandRJamaica.txt:18
./written_2/travel_guides/berlitz1/HandRJerusalem.txt:1
./written_2/travel_guides/berlitz1/HandRLakeDistrict.txt:0
./written_2/travel_guides/berlitz1/HandRLasVegas.txt:0
./written_2/travel_guides/berlitz1/HandRLisbon.txt:0
./written_2/travel_guides/berlitz1/HandRLosAngeles.txt:1
./written_2/travel_guides/berlitz1/HandRMadeira.txt:0
./written_2/travel_guides/berlitz1/HandRMadrid.txt:0
./written_2/travel_guides/berlitz1/HandRMallorca.txt:0
./written_2/travel_guides/berlitz1/HistoryDublin.txt:0
./written_2/travel_guides/berlitz1/HistoryEdinburgh.txt:0
./written_2/travel_guides/berlitz1/HistoryEgypt.txt:0
./written_2/travel_guides/berlitz1/HistoryFWI.txt:0
./written_2/travel_guides/berlitz1/HistoryFrance.txt:0
./written_2/travel_guides/berlitz1/HistoryGreek.txt:0
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:9
./written_2/travel_guides/berlitz1/HistoryHongKong.txt:0
./written_2/travel_guides/berlitz1/HistoryIbiza.txt:0
./written_2/travel_guides/berlitz1/HistoryIndia.txt:0
./written_2/travel_guides/berlitz1/HistoryIsrael.txt:0
./written_2/travel_guides/berlitz1/HistoryIstanbul.txt:0
./written_2/travel_guides/berlitz1/HistoryItaly.txt:0
./written_2/travel_guides/berlitz1/HistoryJamaica.txt:3
./written_2/travel_guides/berlitz1/HistoryJapan.txt:6
./written_2/travel_guides/berlitz1/HistoryJerusalem.txt:0
./written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt:0
./written_2/travel_guides/berlitz1/HistoryLasVegas.txt:1
./written_2/travel_guides/berlitz1/HistoryMadeira.txt:0
./written_2/travel_guides/berlitz1/HistoryMadrid.txt:0
./written_2/travel_guides/berlitz1/HistoryMalaysia.txt:0
./written_2/travel_guides/berlitz1/HistoryMallorca.txt:1
./written_2/travel_guides/berlitz1/IntroDublin.txt:0
./written_2/travel_guides/berlitz1/IntroEdinburgh.txt:0
./written_2/travel_guides/berlitz1/IntroEgypt.txt:0
./written_2/travel_guides/berlitz1/IntroFWI.txt:0
./written_2/travel_guides/berlitz1/IntroFrance.txt:0
./written_2/travel_guides/berlitz1/IntroGreek.txt:0
./written_2/travel_guides/berlitz1/IntroHongKong.txt:0
./written_2/travel_guides/berlitz1/IntroIbiza.txt:0
./written_2/travel_guides/berlitz1/IntroIndia.txt:1
./written_2/travel_guides/berlitz1/IntroIsrael.txt:0
./written_2/travel_guides/berlitz1/IntroIstanbul.txt:0
./written_2/travel_guides/berlitz1/IntroItaly.txt:0
./written_2/travel_guides/berlitz1/IntroJamaica.txt:1
./written_2/travel_guides/berlitz1/IntroJapan.txt:2
./written_2/travel_guides/berlitz1/IntroJerusalem.txt:0
./written_2/travel_guides/berlitz1/IntroLakeDistrict.txt:0
./written_2/travel_guides/berlitz1/IntroLasVegas.txt:0
./written_2/travel_guides/berlitz1/IntroLosAngeles.txt:0
./written_2/travel_guides/berlitz1/IntroMadeira.txt:0
./written_2/travel_guides/berlitz1/IntroMadrid.txt:0
./written_2/travel_guides/berlitz1/IntroMalaysia.txt:0
./written_2/travel_guides/berlitz1/IntroMallorca.txt:0
./written_2/travel_guides/berlitz1/JungleMalaysia.txt:0
./written_2/travel_guides/berlitz1/WhatToDublin.txt:0
./written_2/travel_guides/berlitz1/WhatToEdinburgh.txt:0
./written_2/travel_guides/berlitz1/WhatToEgypt.txt:1
./written_2/travel_guides/berlitz1/WhatToFWI.txt:3
./written_2/travel_guides/berlitz1/WhatToFrance.txt:0
./written_2/travel_guides/berlitz1/WhatToGreek.txt:0
./written_2/travel_guides/berlitz1/WhatToHawaii.txt:0
./written_2/travel_guides/berlitz1/WhatToHongKong.txt:1
./written_2/travel_guides/berlitz1/WhatToIbiza.txt:0
./written_2/travel_guides/berlitz1/WhatToIndia.txt:0
./written_2/travel_guides/berlitz1/WhatToIsrael.txt:0
./written_2/travel_guides/berlitz1/WhatToIstanbul.txt:0
./written_2/travel_guides/berlitz1/WhatToItaly.txt:0
./written_2/travel_guides/berlitz1/WhatToJamaica.txt:3
./written_2/travel_guides/berlitz1/WhatToJapan.txt:4
./written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:0
./written_2/travel_guides/berlitz1/WhatToLasVegas.txt:1
./written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:1
./written_2/travel_guides/berlitz1/WhatToMadeira.txt:0
./written_2/travel_guides/berlitz1/WhatToMalaysia.txt:0
./written_2/travel_guides/berlitz1/WhatToMallorca.txt:2
./written_2/travel_guides/berlitz1/WhereToDublin.txt:1
./written_2/travel_guides/berlitz1/WhereToEdinburgh.txt:0
./written_2/travel_guides/berlitz1/WhereToEgypt.txt:0
./written_2/travel_guides/berlitz1/WhereToFWI.txt:0
./written_2/travel_guides/berlitz1/WhereToFrance.txt:0
./written_2/travel_guides/berlitz1/WhereToGreek.txt:0
./written_2/travel_guides/berlitz1/WhereToHawaii.txt:1
./written_2/travel_guides/berlitz1/WhereToHongKong.txt:0
./written_2/travel_guides/berlitz1/WhereToIbiza.txt:0
./written_2/travel_guides/berlitz1/WhereToIndia.txt:0
./written_2/travel_guides/berlitz1/WhereToIsrael.txt:0
./written_2/travel_guides/berlitz1/WhereToIstanbul.txt:0
./written_2/travel_guides/berlitz1/WhereToItaly.txt:1
./written_2/travel_guides/berlitz1/WhereToJapan.txt:9
./written_2/travel_guides/berlitz1/WhereToJerusalem.txt:0
./written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt:0
./written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:1
./written_2/travel_guides/berlitz1/WhereToMadeira.txt:0
./written_2/travel_guides/berlitz1/WhereToMadrid.txt:0
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt:1
./written_2/travel_guides/berlitz1/WhereToMallorca.txt:0
```
In this example, I used '-c' option again for 'grep' command.
The option counts the number of occurences of the string, "US" and prints it out.
As shown in the output, string "US" shows up in files such as WhereToLosAngeles.txt. It also denotes how many times
the string appears in the file. For instance, "US" appears 1 time in WhereToHawaii.txt.

Usage)
The usage of option '-c' is that it not only tells the user in which files the specific string is 
but also denotes how many times it shows up in each file.
The reason '-c' command is useful is because it works like a search engine that promptly extracts demanded information
from a big data. It hugely alleviates the pain of manual labor, since it would take a long time for the user 
to manually count how many times the word appears.

Reference: 'man grep' command, ChatGPT


## Option 3 : **-i**
> 2 examples of using **-i** on files from ./written_2

Example 1)
```
# Command
grep -i "canada" ./written_2/travel_guides/berlitz1/*

# Output
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Canada); fax 957-5289; e-mail <info@breezes.com>; website
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        953-9153, 800-330-8272 (toll-free from US and Canada); fax 953-2244;
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Tel. 993-2602, 993-2705, 800-633-3284 (toll-free from US or Canada);
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Tel. 965-3145, 965-3185, 800-OUTPOST (toll-free from US and Canada);
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Andrew’s; Tel. 944-8400, 800-OUTPOST (toll-free from US and Canada);
./written_2/travel_guides/berlitz1/HandRMadrid.txt:        in the U.S. and Canada, or 91/521 28 57; fax 91/532 87 76; web site
./written_2/travel_guides/berlitz1/HandRMadrid.txt:        800/325-3535 in the U.S., 800/325-3589 in Canada, or 91/360 80 00; fax
./written_2/travel_guides/berlitz1/HistoryFWI.txt:        Canada to the British.
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        Canada, and Australia from Waikiki, millions fell under the spell of a
./written_2/travel_guides/berlitz1/HistoryHongKong.txt:        were prompted to apply for citizenship elsewhere, notably in Canada and
./written_2/travel_guides/berlitz1/HistoryJapan.txt:        thought to be worth more than the entire real-estate value of Canada.
./written_2/travel_guides/berlitz1/WhereToFrance.txt:        Memorials in the Square du Canada and the beautiful
```
In this example, I used '-i' option for 'grep' command.
The option innitiates a case-insensitive matching to the string I typed in the command (canada).
That means it would look for a string "canada" regardless of its case and print out the corresponding lines.
The result is displayed above as expected. (string in the file is "Canada", not "canada" but was still printed out)

Example 2)
```
# Command
grep -i "manley" ./written_2/travel_guides/berlitz1/*

# Output
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Hedonism II ❁❁❁❁❁ (AI) Norman Manley Blvd. , P.O. Box 25,
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Negril Tree House Resort ❁❁-❁❁❁ Norman Manley Boulevard,
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Sandals Negril Beach Resort and Spa ❁❁❁❁❁ (AI) Norman Manley
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Swept Away Hotel ❁❁❁❁❁ (AI) Norman Manley Boulevard, P.O.
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Errol’s Sunset Café ❁-❁❁ Norman Manley Boulevard, Negril.
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Kuyaba ❁❁ Norman Manley Boulevard, Negril; Tel. 957-4318.
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Margueritaville Bar and Grill ❁❁-❁❁❁ Norman Manley
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Negril Tree House ❁❁-❁❁❁ Norman Manley Boulevard, Negril;
./written_2/travel_guides/berlitz1/HistoryJamaica.txt:        People’s National Party (PNP), led by Norman Manley in opposition to
./written_2/travel_guides/berlitz1/HistoryJamaica.txt:        change in the economic power of the people. Michael Manley, son of
./written_2/travel_guides/berlitz1/HistoryJamaica.txt:        closer to independent nonaligned countries. Manley was made out to be a
./written_2/travel_guides/berlitz1/WhatToJamaica.txt:        depiction was designed and sculpted by Edna Manley.
./written_2/travel_guides/berlitz1/WhatToJamaica.txt:        Manley, one of the foremost modern artists on the island and wife of
./written_2/travel_guides/berlitz1/WhatToJamaica.txt:        Norman Manley, former Prime Minister. Beside the docks is Victoria
./written_2/travel_guides/berlitz1/WhatToJamaica.txt:        the park, and both Marcus Garvey and Norman Manley are buried here.
./written_2/travel_guides/berlitz1/WhereToDublin.txt:        life, the poet Gerard Manley Hopkins lectured here. One of the
```
In this example, I used '-i' option again for 'grep' command.
The option innitiates a case-insensitive matching to the string I typed in the command (manley).
That means it would look for a string "manley" regardless of its case and print out the corresponding lines.
The result is displayed above as expected. (string in the file is "Manley", not "manley" but was still printed out)

Usage)
The usage of option '-i' is that it finds and prints out the lines where the string is in
regardless of its case.
The reason '-i' command is useful is because even if I don't match the case of the string to the way it is in files 
at all, the results that I intended to get still comes out.
It gets rid of the users' pain to match the case of every single letter in the string.

Reference: 'man grep' command, ChatGPT


## Option 4 : **-m num**
> 2 examples of using **-m num** on files from ./written_2

Example 1)
```
# Command
grep -m 2 "Boulevard" ./written_2/travel_guides/berlitz1/*

# Output
./written_2/travel_guides/berlitz1/HandRIsrael.txt:        Alhambra ❁❁❁ 30 Jerusalem Boulevard, Jaffa; Tel. (03) 683
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Negril Tree House Resort ❁❁-❁❁❁ Norman Manley Boulevard,
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        Boulevard, P.O. Box 12, Negril; Tel. 957-5216, 800-SANDALS (toll-free
./written_2/travel_guides/berlitz1/WhatToIsrael.txt:        of Art, Shaul Hamelech Boulevard (tel. 03-696 1297). The Israel Ballet
./written_2/travel_guides/berlitz1/WhatToIsrael.txt:        the Philip Murray Centre, Ha’Temarim Boulevard, and there is a Creat
./written_2/travel_guides/berlitz1/WhatToJamaica.txt:        culture of the island. The National Gallery, on Ocean Boulevard, has a
./written_2/travel_guides/berlitz1/WhatToLasVegas.txt:        2000 Las Vegas Boulevard South; Tel. (702) 380-7777. Shows 7 and 10pm,
./written_2/travel_guides/berlitz1/WhatToLasVegas.txt:        Casino, 3570 Las Vegas Boulevard South; Tel. (702) 731-7110. Multiple
./written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:        Brea (the blocks between Wilshire and Melrose) and Beverly Boulevard
./written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:        Sunset Boulevard’s Sunset Plaza is another stretch of hip
./written_2/travel_guides/berlitz1/WhereToDublin.txt:        return here to browse the “Boulevard Galleries” of art set up around
./written_2/travel_guides/berlitz1/WhereToFWI.txt:        formal fish market is farther along the fascinating canalside Boulevard
./written_2/travel_guides/berlitz1/WhereToFrance.txt:        The Boulevard des Capucines and the Boulevard des Italiens,
./written_2/travel_guides/berlitz1/WhereToFrance.txt:        Lapin Agile. On the Boulevard de Clichy below, the Pigalle district is
./written_2/travel_guides/berlitz1/WhereToJapan.txt:        ginkgo and sycamore trees line the impressive Midosuji Boulevard. This
./written_2/travel_guides/berlitz1/WhereToJapan.txt:        Theater (at the bottom of Midosuji Boulevard) gives kabuki performances
./written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:        Hollywood Boulevard. In fact, the only stars here now are those inlaid
./written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:        stretch for a total of 31⁄2 miles (51⁄2 km) along Hollywood Boulevard
```
In this example, I used '-m num' option for 'grep' command.
The option searches for the string "Boulevard" until it is found twice (since I typed in '2' as num) and prints it out.
The result is displayed above as expected. 
(there are multiple "Boulevard"s in some files but only the first two lines with "Boulevard" are printed out)

Example 2)
```
# Command
grep -m 1 "credit" ./written_2/travel_guides/berlitz1/* 

# Output
./written_2/travel_guides/berlitz1/HandRHongKong.txt:        major credit cards. A 10% service charge and 5% government tax will be
./written_2/travel_guides/berlitz1/HandRJamaica.txt:        mirrored ceilings above the beds. 280 rooms. Major credit cards.
./written_2/travel_guides/berlitz1/HandRJerusalem.txt:        where noted, all hotels listed below accept major credit cards.
./written_2/travel_guides/berlitz1/HandRLasVegas.txt:        All hotels in Las Vegas accept all major credit cards (Visa,
./written_2/travel_guides/berlitz1/HandRLosAngeles.txt:        available from 2pm to 3pm. All hotels accept major credit cards.
./written_2/travel_guides/berlitz1/HandRMadeira.txt:        VAT (value-added tax). All hotels accept major credit cards. For making
./written_2/travel_guides/berlitz1/HandRMadrid.txt:        surprisingly spacious. 27 rooms. Major credit cards.
./written_2/travel_guides/berlitz1/HistoryIndia.txt:        As a result, Gradualist reform became discredited and civil
./written_2/travel_guides/berlitz1/HistoryJamaica.txt:        with impunity. They agreed; Modyford issued letters of accreditation
./written_2/travel_guides/berlitz1/HistoryMadrid.txt:        took credit for a rousing naval victory at Lepanto, teaming with
./written_2/travel_guides/berlitz1/WhatToDublin.txt:        tourist-oriented shops take the VAT off credit-card purchases before
./written_2/travel_guides/berlitz1/WhatToFWI.txt:        of the major credit cards.
./written_2/travel_guides/berlitz1/WhatToGreek.txt:        sculpture, pottery, or icons. They will require proper accreditation,
./written_2/travel_guides/berlitz1/WhatToHongKong.txt:        a credit card, he may then boost the price in order to cover the card
./written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:        simply must have — are all at your disposal with a flash of the credit
./written_2/travel_guides/berlitz1/WhereToFWI.txt:        books, is credited with abolishing slavery here. Another midtown
./written_2/travel_guides/berlitz1/WhereToFrance.txt:        credited with much of the 13th-century construction. During the 18th
./written_2/travel_guides/berlitz1/WhereToHongKong.txt:        there’s no need to change currency. Some places take credit cards, but
./written_2/travel_guides/berlitz1/WhereToIstanbul.txt:        library of over 200,000 volumes (the Pergamenes are credited with the
./written_2/travel_guides/berlitz1/WhereToItaly.txt:        in the Bargello); St. Mark, whose vividly sculpted robes do credit to
./written_2/travel_guides/berlitz1/WhereToJapan.txt:        credited with planting the seeds from which cultural, aesthetic, and
./written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:        records. The building’s distinctive design is credited to recording
./written_2/travel_guides/berlitz1/WhereToMadrid.txt:        settled in the area and are credited with having sculpted the crude
```
In this example, I used '-m num' option again for 'grep' command.
The option searches for the string "credit" until it is found once (since I typed in '1' as num) and prints it out.
The result is displayed above as expected. 
(there are multiple "credit"s in some files but only the first line with "credit" is printed out)

Usage)
The usage of option '-m num' is that it stops reading the file after num matches.
The reason '-m num' command is useful is because it allows the user to access the file content exactly as much as desired.
In a matter of seconds, the user can see in which files the specific word was used and how the word was used up to x amount 
of times (that the user sets up to be) .

Reference: 'man grep' command, ChatGPT
