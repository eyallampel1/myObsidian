# SED - linux search and replace

## What is sed ? 
sed is used to perform basic text transformations on an input stream (a file or input from a pipeline).
It searches for a specific pattern and can replace it with another one 

## Running sed 
a normal sed program looks like this : 
```shell
sed SCRIPT INPUTFILE...
```

For example, to replace all occurrences of ‘hello’ to ‘world’ in the file input.txt:

```shell
sed 's/hello/world/' input.txt > output.txt
```

