<div align="center">
<h1>pactl-vol</h1>
<p>A stupid simple BASH script to handle pactl volume operations by arguments</p>
<img src="https://img.shields.io/badge/Shell_Script-121011?logo=gnu-bash&logoColor=white"></img>
<img src="https://img.shields.io/badge/Made%20with-Bash-1f425f.svg"></img>  
<img src=https://img.shields.io/badge/Maintained%3F-yes-green.svg></img>
<img src="https://badge-size.herokuapp.com/wick3dr0se/pactl-vol/master/pactl-vol"></img>  
<a href="https://discord.gg/TstuWvDzXr">
<img src="https://discordapp.com/api/guilds/913584348937207839/widget.png?style=shield"/></a>
</div>

## Installation
### From GitHub
clone the repository
```bash
git clone https://github.com/wick3dr0se/pactl-vol
```
change directory into the folder
```bash
cd pactl-vol
```

## Usage
`pactl-vol` will automatically detect unbalanced speakers & prompt to sync them. the default sink, used by `pactl-vol`, is set with `pactl`
```bash
bash pactl-vol
```

*if no operator (+/-) is supplied, volume will increase by default; if no operand is supplied, volume will change by 10%*

*`pactl-vol` handles volume by percentages, regardless of specification*

### Accepted Arguments

---

```
+<N> ... increase volume by N%
-<N> ... decrease volume by N%
mute ... toggle mute
```

### Examples

---

increase volume by 10%
```bash
bash pactl-vol <10>
```
decrease volume by 25%
```bash
bash pactl-vol <-25>
```
mute volume
```bash
bash pactl-vol <mute>
```

`pactl-vol` can be bound to keys for finer-grained audio control, e.g. —

i3wm config:
```bash
bindsym XF86AudioRaiseVolume exec bash ~/.config/pactl-vol +5
bindsym XF86AudioLowerVolume exec bash ~/.config/pactl-vol -5
bindsym XF86AudioMute exec bash ~/.config/pactl-vol mute
```
