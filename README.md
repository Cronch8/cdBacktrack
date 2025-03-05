# cdBacktrack

Provides a history for your directory navigation such that you can jump around the locations where you have just been.

Currently only bash is supported.

## Usage

As you navigate around it stores a history of locations. Then with `backtrack` (or a keybind if you set that) you go to the prevous directory. Think of it as the back arrow in aa browser.

`advance` is the second function, it works as you'd expect. It goes forward in the directory history.

PS: the `advance` function is made of code that lives in the mortal realm and as such can't predict where you will be in the future.

## Installation

1. Clone the repo

```
git clone https://github.com/Cronch8/cdBacktrack.git
```

2. Source it from the `.bashrc` file

```bash
source /path/to/repo/.cd_backtrack
```

3. Add keybinds also to `.bashrc` (optional but highly recommended)

```bash
bind '"\C-o":"backtrack\n"' # ctrl + o
bind '"\C- ":"advance\n"'   # ctrl + space
```

Feel free to change them.

## Notes

- The history is not persistent across shell sessions. The reason for this being that it makes it trivial to support usage on multiple simultaneus terminal sessions.

### Enviroment variables

- `CDHISTORY` -- the whole history
- `CDHISTORYLENGTH` -- current length of the history
- `CDHISTORYOFFSET` -- your current position in the history

### The Future

- Bugfixes. It's not perfect.
- Persistent history
