# ranma-nyan-widget

A Nyan Cat animated progress bar widget for the macOS menu bar, powered by [ranma](https://github.com/typester/ranma).

The cat's position represents a system metric (CPU usage, battery level, or custom input), and the animation speed scales with the metric value.

## Usage

```sh
ranma start --init ./init
```

### Data sources

By default, the widget tracks CPU usage. Use the `--source` flag in the init script to change:

- `cpu` (default) — CPU usage percentage, polled every 2s
- `battery` — Battery charge level, polled every 30s
- `stdin` — Read values (0–100) from stdin

To change the source, edit the `init` script and pass `--source <name>` to the plugin.

## Credits

Nyan Cat was created by [Chris Torres](http://www.prguitarman.com/) (prguitarman). This widget generates a pixel-art homage programmatically and is not affiliated with the original creator.

## License

MIT
