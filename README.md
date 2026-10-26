# so_long

A small 2D top-down game in C. Made as part of the 42 curriculum at Codam.

You play a mouse. Collect all the cheese, then reach the exit. Graphics are handled with [MLX42](https://github.com/codam-coding-college/MLX42).

## Build

You need `cc`, `make`, `cmake` and `glfw`.

```sh
git clone --recurse-submodules https://github.com/rowanverschoor/so_long.git
cd so_long
make
```

## Run

```sh
./so_long maps/base.ber
```

## Controls

| Key | Action |
| --- | --- |
| W A S D or arrow keys | Move |
| Esc | Quit |

The move count is printed in the terminal.

## Map format

Maps are `.ber` files.

```
1111
1EC1
1P01
1111
```

- `1` wall
- `0` floor
- `P` player start
- `C` collectible
- `E` exit

A map must be rectangular, surrounded by walls, and have one player, one exit and at least one collectible. A flood fill checks that every collectible and the exit can be reached. The `maps/fail_*.ber` files show maps that get rejected.

## Author

- [roversch](https://github.com/rowanverschoor)
