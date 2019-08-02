# tmux

## install tmux

```
sudo pacman -S tmux
```

## ~/.tmux.conf

```
ln -s ~/.config/tmux/tmux.conf ~/.tmux.conf
```

## Cheat sheet

### Sessions

* Movement
	* `<C-a>s` - list sessions
	* `tmux switch [-t name]` (`:switch`) - switches to an existing session
	* `tmux as [id] [-t name]` (`:attach`) - attaches to an existing session
	* `<C-a>c` (`:detach`) - detach the currently attached session
* Management
	* `tmux new [-s name] [cmd]` (`:new`) - new session
	* `tmux kill-session [-t name]` (`:kill-session`)
	* `<C-a>$` - rename session

### Windows

* Movement
	* `<C-a>w` - choose window from a list
	* `<C-a>[i]` (`:selectw -t [i]`) - go to window `[i]`
	* `<C-a>l` - go to last window
	* `<C-a>p` - go to previous window
	* `<C-a>n` - go to next window
* Management
	* `<C-a>c` (`:neww [-n name] [cmd]`) - new window
	* `<C-a>T` - rename window
	* `<C-a>,` - rename window
	* `<C-a>w` - list all windows
	* `<C-a>f` - find window by name
	* `<C-a>.` - move window to another session (promt)
	* `:movew` - move window to next unused number
	* `<C-a>&` (`:kill-window`) - kill window
		
### Panes

* Movement
	* (o) `<C-a><Tab>` (`:selectp -t :.+`) - move cursor to the next pane
	* `<C-a><Up>` (`:selectp -U`) - move cursor to the pane above
	* `<C-a><Down>` (`:selectp -D`) - move cursor to the pane below
	* `<C-a><Left>` (`:selectp -L`) - move cursor to the pane to the left
	* `<C-a><Right>` (`:selectp -R`) - move cursor to the pane to the right
	* `:selectp [i]` - move cursor to the pane `[i]`
	* `<C-a>q` - move cursor to the pane by number
* Management
	* `<C-a>%` - split current pane vertically
	* `<C-a>"` - split current pane horizontally
