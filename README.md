# Table of Contents

- [Introduction](#Introduction)
- [Get information](#Get-information)
	-[Hardware](#Hardware)
	- [Debugging](#Debugging)
		- [journalctl](#jounalctl)
		- [coredump](#coredump)
	- [Graphics](#Which-graphics-is-running-atm?)
- [After-a-reinstall](#After-a-reinstall)
	- [Lutris](#Lutris)

# Introduction

This is WIP! Here are some commands than can be helpful when using linux. Also some advices here and there. Im farely new to linux, if you find mistakes it would be nice if you tell me.


# Get-information

This section is all about on how to get informations about your system.

## Hardware

Mainboard Info:

`sudo dmidecode -t 2`

## Debugging

### journalctl

The journal collects all kind of massages from the system. Refer to this if you want to know whats going on in your system.

**Use**:
`journalctl`
Options (Highly advice you use --since (hh:mm) otherwise its too much).

Some options: Highly advice you use --since (hh:mm) otherwise its too much).

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
