# PyTest-Practice

This environment helps you check testcases against a Python program of choice.
It has been created to help with Hackerrank and Leetcode practice.

One key feature is that inputs are naturally converted into Python variables as if they were parsed by an interpreter, instead of being passed in via strings.

This tool automatically converts types, which is a big improvement over the `input()` function that passes everything in string form.
You save time on converting stuff and spend more time on honing your algorithmic prowess!

Simply fill up the `input` and `output_expected` directories with input testcases and expected outputs of your own choosing. I have populated them with example files and their outputs as proof that this suite works.

Use Python syntax to denote any kind of variable, as if you were typing into a program. Don't worry about keeping spaces consistent in between elements in lists, or your choice of quotes, etc as the parser will take care of cleaning inputs.
1D and 2D lists are supported as input variables, but don't try this with any greater dimensions.

## Input Files

Input files can have multiple lines, and every variable on each line is combined into a list and passed into your program (the `main` function in `main.py`.)

### Example:

An input file that is:

```
"'weew'd"
'abc'
  123
456.78
[[1,3,"3"],[7  ,9 , 11]]
```

Will be parsed into your program as such:

```
["'weew'd", 'abc', 123, 456.78, [[1, 3, '3'], [7, 9, 11]]]
```

Access this in the `inputs` list that is passed into the `main` function.

Note that all this data is automatically typed! You can see for yourself in the example debug output of this repo.

## Expected Output Files

This suite checks the return output of your program against your expected output. The `output_expected` files are parsed similarly to the input files. _The only difference is, expected outputs only support a single line, just like most Python questions return a single line._
Again, your expected output is parsed like Python syntax, so don't worry about choice of quotes, spaces, etc!
Also, everything is logged to the `log.txt` file in the home directory.

## Other Technical Details

- I have included some draft files from the planning progress in the `draft` folder, they aren't used in the program.
- Most of the suite is in the `main.py`, where your program resides, and the `test.py` file which automates the testing
- I was inspired by the our Compilers module and wanted to apply our newly learnt knowledge in language processing via parsers and lexers.
- I am using the PLY library, a Python implementation of lex and yacc. For more info, check out the repo [here](https://github.com/dabeaz/ply).

Happy hacking!
