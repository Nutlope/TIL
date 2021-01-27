# TIL - New things I'm learning

New things I'm learning and issued I run into in programming.

### 1. Carriage Returns and Line feeds.

Windows machines still have carriage return + line feed (\r\n) to end a new line while unix based systems have standerdized upon just line feed (\n)

### 2. Character Encoding
   ANSI
   ascii
   unicode (UTF-8 vs UTF-8 w/ Signature)  
   UTF-8 with signiture has a BOM (3 bytes in the beginning)

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