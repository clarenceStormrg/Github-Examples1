## Git hidden folder

there is a hidden folder called `.git` which tells you that
our project is a git repo.

If we wanted to create a git repo in a new project we' create the
folder and the initialize that repo using `git init`

```
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch Readme.md
code Readme.md
git status
git add Readme.md
# makes changes to readme.md
git commit -a -m "add readme file"
```

## Cloning

we can clone three ways: HTTPS, SSH, Github CLI

Since we are using Github Codespaces we'll a create
a temporary directory in our workspace

```sh
mkdir /workspace/tmp
cd /workspace/tmp
```

## HTTPS

```sh
 
cd Github-Examples1
```

> You will need to generate a Personal Access Token (PAT)

https://github.com/settings/token

You will use the PAT as your pasword when you login

- Give it access to Contens for Commits

## SSH

```ssh
git@github.com:clarenceStormrg/Github-Examples1.git
cd Github-Examples1
```

We will need to create our own SSH rsa key pair

```sh
sshe-keygen -t rsa
```

For WSL user and if you create a non default key you might need to add it

```sh
eval `ssh-agent`
ssh-add /home/andrew/.ssh/alt-github_id_rsa
```

We can test our connection here:

```
sshe -T git@github.com
```

## Github CLI

Install the CLI

## Commits

When we want to commit code we can write git commit which will open
up the commit edit message in the editor of choice.

```
git commit
```

Set the global editor

```
git config --global core.editor emacs
```

Make a commit and a commit message without opening an editor

```sh
git commit -m "add another exclamation"
```

## Branches

## Remotes

## Stashing

## Merging

## Add

when we want to stage changes that will be included in the commit
We can use the . to add all possible files .

```
git add Readme.md
git add .
```

## Reset

Reset allows you to move Staged changes to be unstaged.
This is useful when you to revert all files not to be not commited.

```
git add .
git reset
```

> git reset will revert a git add.

## Status

Git status shows you what files will or will not be commited

```
git status
```

## Gitconfig file

the gitconfig file is what stores your global configurations for
git such as email, name, editor and more.

showing the contents of our .gitconfig file

```
git config --list
```

When you first install Git on a machine you are suppose to set up
your name and email

```sh
git config --global user.name "clarenceStormrg"
git config --global user.email gutierrezterronesma@gmail.com
```

## Log

git log will show recent git commits to the git tree

## Push

When we want to push a repo to our remote origin

```
git push
```