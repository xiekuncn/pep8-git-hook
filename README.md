PEP8 Git Commit Hook
====================

This is a pre-commit hook for Git that checks the code to be committed
for Python PEP8 style compliance.  The hook will prevent the commit in
case style violations are detected.

Installation:

1. Install the pep8 program: ```$ pip install pep8```
2. Save pre-commit as your_project/.git/hooks/pre-commit
3. Mark pre-commit executable: ```$ chmod +x your_project/.git/hooks/pre-commit```

The hook can be overridden: ```$ git commit --no-verify```

Currently, the following PEP8 codes are ignored for:

E501 line too long (82 > 79 characters)
E402 E402 module level import not at top of file
E731 do not assign a lambda expression, use a def

In case you want to modify the list of codes to ignore, edit the
```ignore_codes``` list in the pre-commit file.   
If you want to select only specific codes to scan for, use the
```select_codes``` list.

This code was forked from [https://gist.github.com/810399](https://gist.github.com/810399).
