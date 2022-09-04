# Git & GitHub

## Config Your Local Machine

1. ### set user name

   ```zsh
   git config --global user.name 'name'
   ```

1. ### set user email

   ```zsh
   git config --global user.email 'email'
   ```

1. ### set other...

   ```zsh
   git config --global core.editor=code --wait
   ```

   ```zsh
   git config --global core.autocrlf=input
   ```

1. ### check config

   ```zsh
   git config --list
   ```

   ```zsh
   git config user.name
   ```

## Git Start

1. ### Git Initializing

   ```zsh
   git init
   ```

1. ### Git Staging [Track]

- only single file

  ```zsh
  git add file name
  ```

- stage all changed file in directory and subdirectory

  ```zsh
  git add --all
  ```

- shorthand for --all [using latter]

  ```zsh
  git add -A
  ```

- stage all changed file in directory but not subdirectory

  ```zsh
  git add *
  ```

- stage all changed file in directory but not subdirectory

  ```zsh
  git add .
  ```

- directory wildcard

  ```zsh
  git add *.js
  ```

- directory and subdirectory wildcard

  ```zsh
  git add **/*.js
  ```

1. ### Git UnStaging [Untrack]

- file name are same like track

  ```zsh
  git rm --cached file
  ```

  ```zsh
  git rm -f --cached file
  ```

  ```zsh
  git rm -r --cached file
  ```

  ```zsh
  git rm -rf --cached file
  ```

1. ### Show changes between commits, commit and working tree, etc

   ```zsh
   git diff
   ```
   
   ```zsh
   git diff --staged
   ```   

1. ### discard changes in working directory

   ```zsh
   git restore file
   ```

1. ### local repository [commit]

- For Moving staging to local repository we can use following command [message should be clear and understandable]

  ```zsh
  git commit -m 'message here'
  ```

- Staging and commit directly

  ```zsh
  git commit -am 'message here'
  ```

1. ### to see the commit history

   ```zsh
   git log
   ```

   ```zsh
   git log --oneline
   ```

1. ### how to uncommit

- if all you want to do is undo the act of committing, leaving everything else intact

  ```zsh
  git reset --soft HEAD^
  ```

- if all you want to do is undo the act of committing, and also removing from the stagging area

  ```zsh
  git reset HEAD^
  ```

- If you actually want to completely undo it, <b> throwing away all uncommitted change, resetting everything to the previous commit <b> [as the original question asked]

  ```zsh
  git reset --hard HEAD^
  ```

1. ### show commit HEAD

   ```zsh
   git show
   ```

   ```zsh
   git show <commit_id>
   ```

   ```zsh
   git show HEAD
   ```

   ```zsh
   git show HEAD~[number]
   ```

1. ### undo modified & commit log change

   ```zsh
   git checkout file
   ```

   ```zsh
   git checkout commit-id
   ```

1. ### you need ignore file and folder create <b>.gitignore</b> file

```zsh
 .env
 *.txt
 !main.txt
 list?.txt
 node_modules/
```
