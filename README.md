# git-ssh
---------

Using git-remote configuration to perform SSH tasks.

Consider this:

```shell
# from within your git repository
$ git remote add web1 user@web1:/var/www/html
$ git ssh web1 pwd -P
```

is the same as running:

```shell
$ ssh user@web1
$ cd /var/www/html
$ pwd -P
```

### Features

- `git-ssh` supports all [SSH options](http://linuxcommand.org/man_pages/ssh1.html), including pseudo-tty (`-t`/`-T`)
- As long as the git remote is ssh-able, `git-ssh` will work. Supported git protocols are: `ssh://`, `git+ssh://`, `host:directory`
- when no command is provided, `git-ssh` will open a remote shell in the designated directory.

### Usage

```shell
git ssh [ssh options] <remote> [<command>]
```
