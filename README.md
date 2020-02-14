# Python Guide
A list of confusing things made simple. Made as I learn.

## List indices

You see a lot of different list index styles. For example:
```
my_list[3]
my_list[1:2]
my_list[::4]
my_list[3::2]
my_list[1:2:3]
```
All of these are valid, but what do they mean? It's actually very simple.

When using list indices, the list takes 3 arguments:
```
my_list[start:end:step]
```
```start``` is where you start, ```end``` is where you end (exclusive), and ```step``` is how big your steps are (every number, every other number, etc.)

It turns out that you can leave any of these blank, and it will still work. For example, if you want to just define the step size, that's when you do something like:

```
my_list[::2]
```

This above code will count from normal start to normal end, but only going every other item. Likewise, if you just want to define an end point, you can do:

```
my_list[:3]
```

which will print out the first three items (0, 1, 2). Of course, if you want to be extra confusing, you could do:

```
my_list[:3:]
````

which will print out the same exact thing, since the third argument is still blank. 

The takeaway is that the colons are only there to separate the arguments, allowing you to specify which argument(s) you are passing in. It's kind of like

```
my_function(arg1, arg2, arg3)
```

except the args are separated by the colons rather than commas.
