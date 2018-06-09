# i3empty

Quickly switch to a new numbered workspace.

## i3 config

Place these lines in your i3 config for wrap-around switching:

```
# Move to a new empty workspace
bindsym $mod+Ctrl+Left exec --no-startup-id i3empty.py prev
bindsym $mod+Ctrl+Right exec --no-startup-id i3empty.py next

# Move a window to a new empty workspace
bindsym $mod+Shift+Ctrl+Left exec --no-startup-id i3empty.py --move prev
bindsym $mod+Shift+Ctrl+Right exec --no-startup-id i3empty.py --move next

# Move to empty workspace near a given workspace
bindsym $mod+Mod1+1 exec --no-startup-id i3empty.py next 1
bindsym $mod+Mod1+2 exec --no-startup-id i3empty.py next 2
bindsym $mod+Mod1+3 exec --no-startup-id i3empty.py next 3
bindsym $mod+Mod1+4 exec --no-startup-id i3empty.py next 4
bindsym $mod+Mod1+5 exec --no-startup-id i3empty.py next 5
bindsym $mod+Mod1+6 exec --no-startup-id i3empty.py next 6
bindsym $mod+Mod1+7 exec --no-startup-id i3empty.py next 7
bindsym $mod+Mod1+8 exec --no-startup-id i3empty.py next 8
bindsym $mod+Mod1+9 exec --no-startup-id i3empty.py next 9
bindsym $mod+Mod1+0 exec --no-startup-id i3empty.py next 10 
```

## Usage

Run `i3empty.py next` or `i3empty.py prev`.

```
usage: i3empty.py [-h] [-r] [-w] [-s] [-m] [direction] [number]

Switch to an empty numbered workspace.

positional arguments:
  direction       either next (default) or prev
  number          workspace to start searching from (default: current)

optional arguments:
  -h, --help      show this help message and exit
  -r, --relative  use workspace indices, not numbers (default: no)
  -w, --nowrap    if at edge, wrap around to other edge (default: yes)
  -s, --nostrict  numbered workspaces have a numeric name (default: yes)
  -m, --move      move container to new workspace (default: no)
```
