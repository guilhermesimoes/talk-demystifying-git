title: Demystifying Git
author:
  name: Guilherme Simões
style: styles.css
output: index.html

--

# Demystifying Git
## or how I learned not to be afraid of detached head

--

### Commands I expect you to know

* branch

* checkout

* commit

* push

* pull

--

### The Advantages of Git

* Flexible

* Hard to lose track of work

--

### The Problem With Git

* <p>Bad UX</p>

--

### Deleting stuff

* git branch --delete &lt;branch&gt;

* git push origin --delete &lt;branch&gt;

* git checkout -- &lt;file/dir&gt;

* git reset --hard HEAD

-- git-cookbook

-- git-spellbook

--

### Fundamentals

* Commit objects

* References to commit objects

--

### Fundamentals

* Commit objects

* References to commit objects

* ...and that's it!

--

# `git add`

-- working-tree-staging-area

-- amazon-worker

--

### `git add --patch`

Interactively choose what will be committed

* y - yes

* n - no

* s - split

* q - quit

--

# `git commit`

--

### `git commit`

Creates a new commit object where

<div class='commit-id-equation'>
  <span class='id'>
    ID
  </span>
  <span class="equals">
    =
  </span>
  <div class='sum'>
    <span>content</span>
    <span>+</span>
    <span>message</span>
    <span>+</span>
    <span>author</span>
    <span>+</span>
    <span>date</span>
    <span>+</span>
    <span>previous commit ID</span>
  </div>
</div>
--

# Commits never change

--

# But we can rewrite history

--

# `git tag`

--

# `git branch`

--

# HEAD

-- snow-trail-map

--

# `git checkout`

-- detached-head

--

# `git stash`

--

# `git remote`

--

# `git fetch`

--

# origin/master vs origin master

--

### origin/master vs origin master

Think of commands as functions

--

### origin/master vs origin master

Some functions receive two arguments:

gitPush(remote, branch)

git push origin master

--

### origin/master vs origin master

Some functions receive one argument:

gitReset(reference)

git reset origin/master

--

### origin/master vs origin master

You still gotta know which is which.

--

### origin/master vs origin master

You still gotta know which is which.

But usually the remote (origin) is implicit.

--

# `git reset`

--

### References / Labels

* commit hash

* tag

* branch

* remote/branch

* HEAD

* stash

--

### Modifiers

* ^

* ~1

--

### Modifiers +

* ~3

* ^^^

* ~2^

* ~2~1

--

### Implications

--

### Implications

* <p>Everything is a reference</p>

--

### Implications

* Everything is a reference

* Every command accepts a reference

-- git-references-exercise

--

# `git merge`

--

# Rewriting history

--

### `git commit --amend`

Allows "changing" the last commit

--

### `git commit --amend`

Allows "changing" the last commit

(It's actually rewriting history!)

--

# `git reflog`

--

# `git rebase`

-- fight

<div class='oponents'>
  <h1>merge</h1>
  <h1>rebase</h1>
</div>

-- merge-problem

--

### `merge vs rebase`

* <p>Depends on team workflow</p>

--

### `merge vs rebase`

* Depends on team workflow

* There's no best approach

--

### `merge vs rebase`

* Depends on team workflow

* There's no best approach

  (though it's clearly rebase)

--

### References

* [Learn Git Branching](http://learngitbranching.js.org/)

* [Git For Ages 4 And Up](https://www.youtube.com/watch?v=1ffBJ4sVUb4)

* [Classic Programmer Paintings](http://classicprogrammerpaintings.com/)

--

git reflog expire --expire-unreachable=now --all

git gc --prune=now
