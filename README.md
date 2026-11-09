# Python Week 6 - Safe Functions

This project shows how to stop a Python program from crashing when something goes wrong.

## Files

- `safe_tools.py` - three functions that handle errors with `try` / `except`.
- `README.md` - this file.

## How it works

1. `safe_divide(a, b)` divides two numbers. If `b` is 0, it returns `Cannot divide by zero`.
2. `safe_number(text)` turns text into a whole number. If it can't, it returns `Not a number`.
3. `get_field(learner, key)` looks up a key in a dictionary. If the key is missing, it returns `Field not found`.
4. Each function puts the risky line in `try` and the fallback message in `except`.
5. Each `except` names the exact error it expects, so other bugs are not hidden.

## How to run

Run `python safe_tools.py`. It prints six lines, ending with `Field not found`.

## Why can the `if` check not catch `abc` on its own?

`"abc"` is a valid string, so an `if` check can't tell it will fail until `int()` tries to convert it. `try` / `except ValueError` catches that failure and keeps the program running.