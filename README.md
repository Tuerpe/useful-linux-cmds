# useful-linux-cmds

# Infos
## Debug
### Journalctl

jounalctl collects all kind of massages of the system. Refer to this if you want to know whats going on in your system.

**Use**:
`journalctl`
Options (Highly advice you use --since (hh:mm) otherwise its too much)
`-o short --user --since --no-page(ing) -u [servicename]`

Advice
`journalctl | grep [anything]`

### coredump
**Use**:
`coredumpctl` for showing dumps
`sudo coredumpctl debug [path] (usr/bin/...)`

CoreDump is only availabe if you have build with dcmake_build = Debug.


# Graphics

## Lutris

# DXVK HUD

To enbale the DXVK_HUD: Configure > System options > Environment variables > Add

Key: `DXVK_HUD` Value: `devinfo,fps,frametimes,submissions,drawcalls,pipelines`

## Which graphics is running atm ?

`glxinfo|egrep "OpenGL vendor|OpenGL renderer"`



# After Reinstall

## Lutris

I think for lutris you should delete lutris folder in
`.config`
and
`.local/share`

I think its messing around with wine version and some symlinking or smth. After deleting those he pulled new lutris wine version.
