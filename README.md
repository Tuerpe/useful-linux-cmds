# Table of Contents

- [Introduction](#Introduction)
- [Get information](#Get-information)
	- [Debugging](#Debugging)
		- [journalctl](#jounalctl)
		- [coredump](#coredump)
	- [Graphics](#Which-graphics-is-running-atm?)
- [After-a-reinstall](#After-a-reinstall)
	- [Lutris](#Lutris)

1. List item

# Introduction

# Get-information

This section is all about on how to get informations about your system.

## Debugging

### journalctl

**jounalctl** collects all kind of massages of the system. Refer to this if you want to know whats going on in your system.

**Use**:
`journalctl`
Options (Highly advice you use --since (hh:mm) otherwise its too much).

Some options:
`-o short --user --since --no-page(ing) -u [servicename]`

Advice
`journalctl | grep [anything]`

### coredump
**Use**:
`coredumpctl` for showing dumps
`sudo coredumpctl debug [path] (usr/bin/...)`

CoreDump is only availabe if you have build with dcmake_build = Debug.

## Graphics

### Which-graphics-is-running-atm ?

`glxinfo|egrep "OpenGL vendor|OpenGL renderer"`

# After a reinstall

## Lutris

I think for lutris you should delete lutris folder in
`.config`
and
`.local/share`

I think its messing around with wine version and some symlinking or smth. After deleting those he pulled new lutris wine version.
