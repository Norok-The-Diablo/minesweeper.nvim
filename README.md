![Banner Image](./media/nvimesweeper.png)

![Screenshot](./media/screenshot.png)

Play Minesweeper in Neovim: because if Emacs has taught us anything, it's that
text editors are for gaming!

Requires Neovim version 0.7 or above.

_Note that an `nvim-0.5` branch exists for compatibility with Nvim v0.5+, but it
is no longer maintained._

## How to play

Install it using your favourite package manager like any other plugin, then run
`:Nvimesweeper` and pray that it works properly, I guess.

- Press `!` to flag a square.
- Press `?` to mark a square for later.
- Press `<Space>` or `<RightMouse>` to cycle between `!`, `?` and unmarking a
  square.
- Press `<CR>`, `x` or `<LeftMouse>` to reveal a square; just try not to step on
  a mine!

Run `:help nvimesweeper` for more details.

### Seeding the random number generator

Nvimesweeper does not yet take responsibility for seeding the random number
generator used to place the mines, meaning you may see the same mine layout
after restarting Nvim.

To solve this, you may want to seed the RNG before running `:Nvimesweeper`,
like:

```vim
:lua math.randomseed(os.time())
```

## Why did you make this?

I don't know...
