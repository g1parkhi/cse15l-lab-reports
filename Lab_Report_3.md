# Lab Report 3

## Command

> I will research the **grep** command.

## Option 1 : **-a, --text**
> 2 examples of using **-a, --text** on files and directories from ./written_2

```
# ex1.java Content 
there

gktfuj hi jkgkug

bbbbbb hi cccccc
```

```
# ex2.bin Content 
there

kutfkgt hi gvkuvkjku

jjjjjj hi poopoooo
```

Example 1)
```
# Command
grep -a "hi" ./written_2/*

# Output
./written_2/ex1.java:gktfuj hi jkgkug
./written_2/ex1.java:bbbbbb hi cccccc
```
In this example, I intentionally created a java file (instead of a text file) named 'ex1' under ./written_2.
The **-a** option forces 'grep' to treat all files as text files. 
Since the command basically searches for a specific string ("hi" in this example) from all text files under ./written_2 
and prints out the corresponding lines, the following results are displayed.

Example 2)
```
# Command
grep --text "hi" ./written_2/*

# Output
./written_2/ex2.bin:kutfkgt hi gvkuvkjku
./written_2/ex2.bin:jjjjjj hi poopoooo
```
In this example, I intentionally created a binary file (instead of a text file) named 'ex2' under ./written_2.
The **--text** option forces 'grep' to treat all files as text files. 
Since the command basically searches for a specific string ("hi" in this example) from all text files under ./written_2 
and prints out the corresponding lines, the following results are displayed.

Reference: 'man grep' command, ChatGPT


## Option 2 : **-c**
> 2 examples of using **-c** on files and directories from ./written_2

```
# ex1.java Content 
there

gktfuj hi jkgkug

bbbbbb hi cccccc
```

```
# ex2.bin Content 
there

kutfkgt hi gvkuvkjku

jjjjjj hi poopoooo
```

Example 1)
```
# Command
grep -c "hi" ./written_2/*

# Output
./written_2/ex1.java:2
```
In this example, I created a java file named 'ex1' under ./written_2 just as I did for Option1.
The **-c** option counts the number of occurences of the string, "hi" and prints it out.
The result is displayed above as expected.

Example 2)
```
# Command
grep -c "hi" ./written_2/*

# Output
./written_2/ex2.bin:2
```
In this example, I created a binary file named 'ex2' under ./written_2 just as I did for Option1.
The **-c** option counts the number of occurences of the string, "hi" and prints it out.
The result is displayed above as expected.

Reference: 'man grep' command, ChatGPT


## Option 3 : **-i**
> 2 examples of using **-i** on files and directories from ./written_2

```
# ex1.java Content 
there

gktfuj hi jkgkug

bbbbbb hi cccccc
```

```
# ex2.bin Content 
there

kutfkgt hi gvkuvkjku

jjjjjj hi poopoooo
```

Example 1)
```
# Command
grep -i "HI" ./written_2/* 

# Output
./written_2/ex1.java:gktfuj hi jkgkug
./written_2/ex1.java:bbbbbb hi cccccc
```
In this example, I created a java file named 'ex1' under ./written_2 just as I did for Option1.
The **-i** innitiates a case-insensitive matching to the string I typed in the command.
That means it would look for a string "HI" regardless of its case and print out the corresponding lines.
The result is displayed above as expected. (string in the file is "hi", not "HI" but was still printed out)

Example 1)
```
# Command
grep -i "HI" ./written_2/* 

# Output
./written_2/ex2.bin:kutfkgt hi gvkuvkjku
./written_2/ex2.bin:jjjjjj hi poopoooo
```
In this example, I created a binary file named 'ex2' under ./written_2 just as I did for Option1.
The **-i** innitiates a case-insensitive matching to the string I typed in the command.
That means it would look for a string "HI" regardless of its case and print out the corresponding lines.
The result is displayed above as expected. (string in the file is "hi", not "HI" but was still printed out)

Reference: 'man grep' command, ChatGPT


## Option 4 : **-m num**
> 2 examples of using **-m num** on files and directories from ./written_2

```
# ex1.java Content 
there

gktfuj hi jkgkug

bbbbbb hi cccccc
```

```
# ex2.bin Content 
there

kutfkgt hi gvkuvkjku

jjjjjj hi poopoooo
```

Example 1)
```
# Command
grep -m 1 "hi" ./written_2/ex1.java

# Output
gktfuj hi jkgkug
```
In this example, I created a java file named 'ex1' under ./written_2 just as I did for Option1.
The **-m 1** search for the string "hi" until it is found once (since I typed in '1' as num) and print it out.
The result is displayed above as expected. (there are two "hi"s in file but only the first line with "hi" is printed out)

Example 2)
```
# Command
grep -m 1 "hi" ./written_2/ex2.bin 

# Output
kutfkgt hi gvkuvkjku
```
In this example, I created a binary file named 'ex2' under ./written_2 just as I did for Option1.
The **-m 1** search for the string "hi" until it is found once (since I typed in '1' as num) and print it out.
The result is displayed above as expected. (there are two "hi"s in file but only the first line with "hi" is printed out)

Reference: 'man grep' command, ChatGPT
