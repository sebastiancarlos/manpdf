# 💪📄 ManPDF

Read your Man pages in PDF format.

## Installation

Download the script and make it executable by running:

```shell
curl https://raw.githubusercontent.com/sebastiancarlos/manpdf/main/manpdf --output $HOME/.local/bin/manpdf
chmod +x $HOME/.local/bin/manpdf
```

Make sure that `$HOME/.local/bin` exists and is in your `$PATH`.

## Usage

```shell
<Open a man page as a PDF file>
Usage: manpdf [-o|--output <arg>] [--(no-)open-pdf] [-h|--help] [-v|--version] <name-or-file> [<section>]
	-o, --output: The output file (no default)
	--open-pdf, --no-open-pdf: Open the PDF file after creating it (on by default)
	-h, --help: Prints help
	-v, --version: Prints version
```

## Example

To view the man page for `ls` in PDF format, run:

```shell
manpdf ls
```

## Thanks to
- [Argbash](https://argbash.io/) for generating the CLI parser.
- [Groff](https://www.gnu.org/software/groff/) for generating the PDF.

## Related repositories
- [manpdf-web](https://github.com/sebastiancarlos/manpdf-web): The [website](https://manpdf.pro) for ManPDF.

## License

MIT