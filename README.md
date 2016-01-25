# git-ssh
---------

Convenient helper for git-remote and SSH

Consider this:

```shell
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
- As long as the git remote is ssh-able, `git-ssh` will work. Supported git protocols are: `ssh://`, `git+ssh://`, `host@directory`
- when no command is provided, `git-ssh` will open a remote shell in the designated directory.

### Usage

```shell
git ssh web1 <ssh-options>
git ssh web1 <ssh-options> <command>
```
