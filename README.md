# TIL - Programming

A list of useful programming things I'm learning and issues I fixed.

### 1. Carriage Returns and Line feeds.

Windows machines still have carriage return + line feed (\r\n) to end a new line while unix based systems have standerdized upon just line feed (\n)

### 2. Character Encoding

- ANSI
- Ascii
- Unicode (UTF-8 vs UTF-8 w/ Signature)
- UTF-8 with signiture has a BOM (3 bytes in the beginning)

Resources:

- [Unicode](https://csharpindepth.com/Articles/Unicode)
- [Unicode and Char sets by Joel](https://www.joelonsoftware.com/2003/10/08/_the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/)
- [ANSI vs Utf](https://stackoverflow.com/questions/700187/unicode-utf-ascii-ansi-format-differences)

### 3. Gitignore files

Create a .gitignore file in your current repo if you want to ignore certain files and folders.
Each file/folder should be on a seperate line and folders need to have a / at the end.
To stop tracking a file that is currently tracked, use 'git rm --cached FILENAME'

### 4. VSCode CMD-L not working

CMD-L shortcut to select a line didn't work on Vscode because a live share extension shortcut interfered. Can either delete live share or change the live share keyboard shortcut to get rid of the problem.

### 5. Setting upstream repos

Use "git push --set-upstream <remote> <branch>" to use the <remote> repo as the new default when typing "git push".

### 6. Count the lines in a github repo

$ git ls-files | xargs wc -l
(only caviat is you need to have the files tracked in git)

### 7. Search bash commands you've written in the past.

reverse-i-search: Search backward starting at the current line and moving ‘up’ through the history as necessary. This is an incremental search.

How to use: Press the ctrl key and the r key simultaneously.

### 8. Converting letters to Unicode

When we want to convert letters to unicode or compare between them, we can use the [ord](https://docs.python.org/3/library/functions.html#ord) function in python.

```python
# Example usage:
- ord('A') # 54
- ord('B') - ord('A') # 1
```

### 9. Inverting Binary numbers

To invert numbers, we can use the XOR bitwise operator (^1).

### 10. Backdating git commits

It's possible to backdate git commits by using the --date commit argument.

Example: git commit --date="2004.07.14 13:00" -m "an old commit"

### 11. Python program to exe

Use pyinstaller to do this using the following command: % pyinstaller --onefile 'filename.py'

### 12. Python program to perpetually scroll down

Use pyautogui to do this. Can use this code:

`while True: pyautogui.scroll(-50); pyautogui.time.sleep(0.2)`

### 13. Use VPS to run very long tasks or cron jobs

Use a VPS like Linode or Digital Ocean, spin up an Ubuntu server, and use [nohup](https://unix.stackexchange.com/questions/362115/how-to-keep-a-python-script-running-when-i-close-putty) to run it in the background.

```bash
nohup python myScript.py
```

### 14. Copy files from local to remote ssh server (like a VPS)

```bash
# copy myfile.txt to remote server and place in /remote/server (will place in home if left unspecified).
scp myfile.txt remoteuser@remoteserver:/remote/folder/

# copy everything in current folder to remote server.
scp * remoteuser@remoteserver:/remote/folder/
```

Credit to this [guide](https://www.simplified.guide/ssh/copy-file).

### 15. Debugging python files

Simply insert a "breakpoint()" in the code on a line, which will trigger a built in debugger, Pdb. Then, run your program and step through it using 'n' for next. You can also query variables at any point while stepping through.

More commands can be found [here](https://docs.python.org/3/library/pdb.html)
