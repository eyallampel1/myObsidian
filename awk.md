# AWK - Linux scripting language 
you can use awk command in Linux to filter data, usually std in is a file, std out is your screen

## How is AWK command look like ? 
> pattern { action }

* Example : 
	search in the file named BBS-list for a row containing the word foo (or part of a word) , if found such a row, print the whole row (the print $0 statement)
```shell
awk ’/foo/ { print $0 }’ BBS-list
```

*In an AWK rule, **either the pattern or the action can be omitted**, but not both. If the pattern is omitted, then the action is performed for every input line. If the action is omitted, the default action is to print all lines that match the pattern.



## Print the first column in a file
``` shell
awk '{print $1}' myfile.txt
```
1. $0 = whole row
2. $1 = first column
3. $2= sec column
4. NF = Number of fields(columns) 
5. NR = Number of rows in the file 

*normally the delimiter between fields is a space, but you can change that to something else if you like 

## Print the third and the first column in a file
```shell
awk '{print $3,$1}' myfile.txt
```

## Print the last column in a file

```shell
awk '{print $NF}' myfile.txt
```

## Change the delimiter from the default space to **:** 
```shell
awk -F':' '{print $1,$7}' /etc/passwd
```
## AWK exercises 

1. For the input file `addr.txt`, display all lines containing `is`.
```shell
cat addr.txt 

Hello World 
How are you 
This game is good 
Today is sunny 
12345 
You are funny 
```

```shell
awk '/is/' addr.txt 
This game is good 
Today is sunny
```

2. For the input file `addr.txt`, display all lines containing less than 2 fields.

```shell
awk 'NF<3' addr.txt
Hello World
12345
```

[[nawkA4.pdf]]
