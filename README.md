# 💪📄 ManPDF

Read your Man pages in PDF format.

## Installation

Download the script and make it executable by running:

```shell
curl https://raw.githubusercontent.com/sebastiancarlos/manpdf/main/manpdf -O $HOME/.local/bin/manpdf
chmod +x $HOME/.local/bin/manpdf
```

Make sure that `$HOME/.local/bin` exists and is in your `$PATH`.

## Example

To view the man page for `ls` in PDF format, run:

```shell
manpdf ls
```

## Usage

```shell
manpdf [-o|--output <arg>] [--(no-)open-pdf] [-d|--(no-)debug] [-h|--help] [-v|--version] <name-or-file> [<section>]
        -o, --output: The output file (no default)
        --open-pdf, --no-open-pdf: Open the PDF file after creating it (on by default)
        -d, --debug, --no-debug: Print debug information too (off by default)
        -h, --help: Prints this help
        -v, --version: Prints version
```

## Requirements

ManPDF should work everywhere. The only requirements are:
 - A `man` implementation (`man-db`, `mandoc`, or even that old non-GPL implementation on macOS),
 - `groff`, 
 - `gzip`, to handle distros that compress man pages by default, and
 - `open` or `xdg-open` associated with an application that can open PDFs.

## Troubleshooting

### `groff: fatal error: invalid device 'pdf'`
Some distros come with a `groff` version that doesn't support PDF. For example, Debian and Ubuntu come with the `groff-base` package, which causes the issue `groff: fatal error: invalid device 'pdf'`. To fix this, install the `groff` package:

```bash
sudo apt install groff
```

## Thanks to
- [Argbash](https://argbash.io/) for generating the CLI parser.
- [Groff](https://www.gnu.org/software/groff/) for generating the PDF.

## Related repositories
- [manpdf-web](https://github.com/sebastiancarlos/manpdf-web): The [website](https://manpdf.pro) for ManPDF.

## License

MIT