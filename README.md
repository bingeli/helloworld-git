## 1. create a remote repository
- log in to https://github.com
- name
- do not create readme, then you get a repository without any commit

## 2. install git
- download git from https://git-scm.com/
- install git to path
- config git with your username
```
$ git config --global user.email "bingeli@github.com"
$ git config --global user.name "bingeli"
```

## 3. create local files
- create a folder (better name the same as the remote repository 'helloworld-git')
- create a file 'README.md'
- create a text file 'helloworld.txt', and write helloworld
```
$ tree helloworld-git/
helloworld-git/
├── helloworld.txt
└── README.md
```

## 4. init a local repository
- create a local repository
```
$ git init
Initialized empty Git repository in helloworld-git/.git/
```

## 5. add remote
- link the remote repository to the local repository
```
$ git remote add origin https://github.com/bingeli/helloworld-git.git
(git remote add <remote nickname> <url>)
```

## 6. commit first to local
- check status
```
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.md
        helloworld.txt

nothing added to commit but untracked files present (use "git add" to track)
```
- choose file 'helloworld.txt'
```
$ git add helloworld.txt
(git add <filename>)
```
- commit all the staged files with message 'init: helloworld'
```
$ git commit -m "init: helloworld"
(git commit -m "commit message")
```

## 7. push local to remote
- push the local repository to the remote repository
```
$ git push origin master:master
(git push <repository> <local branch>:<remote branch>)
```