#Mutable vs Immutable Objects

###Mutable
   An object that can be changed after it’s created
### Immutable 
   An object that can not be changed after it’s created

In Java everything except Strings are mutable by default

Every time you change a string, it basically means you are creating a new string, a completely separate copy.
(Only in JAVA Strings are immutable)

So why it String is immutable? It provides caching, synchronization, and performance.

So how it is achieved? As String is a most widely used data structure, Java uses caching to store string literals and reuse them to save heap space. So what does this (caching to store string literals) mean?

```markdown
String s1 = "hello"; 
String s2 = "hello"; 
```

The above two lines point to the same reference/heap space, instead of creating a new heap memory for each variable
If you would like to explicitly create a new memory space for the same string value, then you would need to create a new object
```markdown
String s3 = new String("hello"); 
```