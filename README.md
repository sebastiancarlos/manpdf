# 💪📄 ManPDF & ManWEB 💪🌎

![man-pdf](https://user-images.githubusercontent.com/88276600/230772238-78562f6a-d0ea-4b91-88b1-0b5c52fb7adf.png)

Read your Man pages in PDF format. Even Online!

## Installation

Download the scripts and make them executable by running:

```shell
git clone https://github.com/sebastiancarlos/manpdf
mv manpdf/manpdf $HOME/.local/bin && chmod +x $HOME/.local/bin/manpdf
mv manpdf/manweb $HOME/.local/bin && chmod +x $HOME/.local/bin/manweb
```

Make sure that `$HOME/.local/bin` exists and is in your `$PATH`.

## Example

To view the man page for `ls` in PDF format, run:

```shell
manpdf ls
```

You can download a man page from the web. Fox example, to view the man page for `systemd` in the latest version of Arch, btw, run:

```shell
manweb systemd
````

This also supports PDF

```shell
manweb systemd --pdf
````

## Usage

```shell
manpdf [-o|--output <arg>] [--(no-)open-pdf] [-d|--(no-)debug] [-h|--help] [-v|--version] <name-or-file> [<section>]
	<name-or-file>: You can pass either the name of the man page, a man page file (local or URL), or "-" to read file from stdin
	-o, --output: The output file (no default)
	--open-pdf, --no-open-pdf: Open the PDF file after creating it (on by default)
	-d, --debug, --no-debug: Print debug information too (off by default)
	-h, --help: Prints this help
	-v, --version: Prints version
```

```shell
ManWEB - Open a man page from Manned.org

manweb [-p|--(no-)pdf] [-w|--(no-)where] [-d|--(no-)debug] [-t|--(no-)try-local]
    [-o|--output <arg>] [-h|--help] <name-or-url> [<section>]\n
    <name-or-url>: You can pass either the name of the man page, the URL to a
            manned.org page, or the URL to any raw man page in roff format (hosted at manned.org or not)
    -p, --pdf, --no-pdf: If passed, the script will not open the man page, it will just open it
            as a PDF. (off by default)
    -w, --where, --no-where: Don't actually show the man page, but print the URL of the matching
            page, if found. (off by default)
    -d, --debug, --no-debug: Print debug information too (off by default)
    -t, --try-local, --no-try-local: If there's a local man page available, don't try to fetch
            from network (on by default)
    -o, --output: The output file. If passed, the script will not open the man page, it will just
            save it to disk in roff format. When combined with the --pdf option, it will save the PDF to
            the provided filename. (no default)
    -h, --help: Prints this help
```

## Requirements

ManPDF should work everywhere. The only requirements are:
 - A `man` implementation (`man-db`, `mandoc`, or even that old non-GPL implementation on macOS),
 - `groff`, 
 - `gzip`, to handle distros that compress man pages by default, and
 - `open` or `xdg-open` associated with an application that can open PDFs.

## Thanks to
- [Argbash](https://argbash.io/) for generating the CLI parser.
- [Groff](https://www.gnu.org/software/groff/) for generating the PDF.
- [Manned.org](https://manned.org/) for the best online man pages.

## Related repositories
- [manpdf-web](https://github.com/sebastiancarlos/manpdf-web): The [website](https://manpdf.pro) for ManPDF.

## License

MIT
