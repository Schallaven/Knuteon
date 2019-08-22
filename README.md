# Knuteon

``Knuteon!`` is a small and handy command-line-based application that allows extracting individual data signals from *Karat&nbsp;32* data files. The extracted data signals are then saved as simple text files, which can easily processed by other applications.

``Knuteon!`` is easy to use on any platform that supports Python and also provides some command line parameters to extract specific traces or header information of a data file. The program is released under the GNU General Public License 3 (GPLv3) and I hope that it is of use for the capillary electrophoresis community.

# Usage

Use it like

```bash
$ ./knuteon.py testdata.dat
```
and it will generate text files in the format of testdata._SN_.txt, where _SN_ is the individual signal number. Each text file includes further information of the signal and experiment.

There are some command line parameters available:
```bash
$ ./knuteon.py -h
usage: knuteon.py [-h] [-v] [-a | -f | -i | -t | -e ID] inputfile

Knuteon! This program extracts the data from Karat32 data files.

positional arguments:
  inputfile

optional arguments:
  -h, --help            show this help message and exit
  -v, --version         prints version information
  -a, --all             extracts all detector traces and saves them as files
  -f, --list_files      lists all files and streams in the data file
  -i, --print_header    prints only the header information (chrom header)
  -t, --list_traces     lists all traces in the data file
  -e ID, --extract_trace ID
                        extracts the single trace given by ID and prints it to
                        stdout
```
