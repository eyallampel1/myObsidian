# Regex advanced search 

## what is regex
regex is a programming lang that let you match and find advanced search pattern in text 


## normal searches 
regex can be used to find normal search patterns like any normal text editor 
example : 
![[Pasted image 20221009151439.png]]


## The or \[\] 

^OR-bracket

  
Select One of the characters in the brackets

```regex
[bcr]at > cat or bat or rat
```



[] can be used as range - select One of the characters in the range from x to y

```regex
[A-Z]ba   > Aba Bba ... Zba
```

^theBracketMD

^ inside bracket says not, everything but this character
```regex
[^b]og > match : hog,dog  | skip: bog
```
^the [] markdown

## Escaping with backslash \
If you want to search any special command characters, you need to escape them with backslash 
- example : 
```regex
\w+\.\w+\(\) -> function.doSomthing()
```
## The ? Quantifier - 0 or 1 occurrence 

The ? Sign after a word means 0 or 1 occurrence only , this is the optional character sign
examples: 
	1.
	
```regex
b?og > match : og,bog
```
	2.
	
![[Pasted image 20221017150012.png]]