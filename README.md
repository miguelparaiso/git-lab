# git-lab

> tool for gitlab bulk operations on every project within a group

## install

```sh
npm install -g git-lab
```

## use
```sh
# cd into your desired directory for the gitlab group
mkdir rocket-science && cd rocket-science

# enter token, url and group and save it
git-lab --token 009afdg0SdfAS14250 --url https://gitlab.myserver.com --group rocket-science  --save

# list all repos within the group
git-lab

# clone all repos within the group
git-lab -- clone

# execute actions on all repos (locally)
git-lab -- npm install
git-lab -- mvn install
```


you can also use the help:

```sh
➜ git-lab -h

gitlab tool

usage: git-lab {options} -- {git command} [git options]

options:
 --token, -t gitlab acces token
 --url,   -u gitlab url, e.g: https://gitlab.myserver.com
 --group, -g gitlab group name

example:

 git-lab --token 009afdg0SdfAS14250 --url https://gitlab.myserver.com --group rocket-science  --save -- clone

example with environment variables:

 TOKEN=009afdg0SdfAS14250 URL=https://gitlab.myserver.com GROUP=rocket-science git-lab -s -- clone
```

## license

MIT