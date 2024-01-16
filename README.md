# ist-mario
In this assignment, you will get experience with c's `printf` statement.

## hello.c
Let's remember how to compile and run a program. First, let's `cat` out the contents of `hello.c`

```
cat hello.c
```

This program is using the `printf` function from the `stdio.h` library. `printf` has several special *metacharacters* that control aspects of the output. For now, the metacharacter we are concerned with is `\n`, which prints out a newline. Now compile an run the program.

```
gcc hello.c -o hello
./hello
```

Next, let's use `vim` to edit the program to print out a different message. Open the file using `vim hello.c`. Then place your cursor on the `printf` line. Using vim's change (c) command, we can delete everything inside of the parenthesis and enter exit mode by typing `ci"`. Type in a new message, then exit insert mode with the Escape key. Then save and quit vim with `:wq`. Recompile and rerun your program.

## mario.c
Next, let's create a new file named `mario.c`. You can do so by making a copy of hello.c. This way, we do not need to retype all of the *boiler plate code* and can just focus on editing the file to make changes.

```
cp hello.c mario.c
```

For this assignment, you will build a short tower like Mario climbs before completing a level. Your output should look like this:

```
       #
      ##
     ###
    ####
   #####
  ######
 #######
########
```

Use the *yank* command to copy the `printf` line with `yy`. Next paste the copied line with `p` (or you can paste it multiple times with something like `7p`). Change each `printf` until the output matches the example above.

To compile and run your code, rerun `gcc` on the `mario.c` file.

```
gcc mario.c -o mario
./mario
```

When your program works as intended, use git to update your repository and push your changes to github.

```
git add .
git commit -m "Completed mario assignment"
git push
```

## vim tips
- `yy` - copy entire line
- `p` - paste
- `#p` - paste number of times
- `ci"` - delete inside of parenthesis and enter insert mode
- `i` - enter insert mode
- `R` - enter REPLACE mode
- `escape` - exit insert/replace mode
- `:wq` - save and quit

## Extra practice
Create another program named `asciiart.c`. You can create it from scratch with `vim asciiart.c`, or make a copy of your mario file `cp mario.c asciiart.c`. Write a program that uses `printf` statements to create your own image using ascii characters. Use gcc to compile and run with `./asciiart`. Use the three git commands above to update your repo on GitHub.
