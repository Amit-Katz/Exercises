# Exercise 1

## Summary
We have this cool file: `text.txt`, it's content is:

```
Hello this is very cool
```

In this excersize the goal is to track changes made to this file, create versions, and switch between them.

## Details

When we will run the command:
```bash
python main.py START $TEXT_TXT_PATH
```
The *first* version will be created and saved. Let's say that now we change `text.txt` content to:
```
Hello this is very cool, and awesome
```
and run:
```bash
python main.py VERSION $TEXT_TXT_PATH
```
The *second* version was created!

Finally, if we run:
```bash
python main.py SWITCH $TEXT_TXT_PATH 1
```

The file's content should return back to be:
```
Hello this is very cool
```

and if we run:
```bash
python main.py SWITCH $TEXT_TXT_PATH 2
```

The content should be:
```
Hello this is very cool, and awesome
```

You get the point.

## Instructions and important notes
1. Use python 3 (not python 2)
2. Instead of `$TEXT_TXT_PATH` there should be the full path to a file. Like: `C:\Users\User\Desktop\Folder\text.txt`
3. The commands running are seperate, there is not a "while" loop or something between commands. Each command is a seperate execution of the file `main.py`
4. Think of "edge cases" like: What if we run the command `START` twice? What if we run `SWITCH` to a version that doesn't exists? What is we delete the file?

## Useful stuff

- Use `sys.argv`. Read about what is it. It's what you're looking for.
- Use `os`, It has everying you'll need

__Happy Hacking__