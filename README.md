# PDF Merger Tool

The PDF Merger Tool is a command-line utility designed to merge multiple PDF files into a single PDF. This tool provides options to sort PDFs alphabetically or by last modification time before merging and supports selective merging from a list or an entire directory.

## Prerequisites

- Python 3.x
- `pypdf` library
- Linux or Unix-like operating system for `notify-send` notifications

## Installation

1. **Install Python 3 and pip** (if not already installed):
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip
   ```

2. **Install the `pypdf` library**:
   ```bash
   pip install pypdf
   ```

3. **Clone the repository** (or download the script directly):
   ```bash
   git clone https://github.com/yourusername/pdf-merger.git
   cd pdf-merger
   ```

## Usage

### General Syntax

```bash
python merge.py <command> [options]
```

### Commands

- **all**: Merge all PDFs within a specified directory.
- **select**: Selectively merge specified PDF files.

### Options

- `-a`, `--alpha`: Sort PDF files alphabetically.
- `-l`, `--last-mod`: Sort PDF files by last modification time.
- `-n`, `--name`: Specify the name of the output merged PDF (default is `combined.pdf`).
- `-c`, `--clobber`: Overwrite the output file if it already exists.
- `-d`, `--dest`: Specify the destination path for the merged PDF.

### Examples

1. **Merge all PDFs in a directory, sorted by last modification**:
   ```bash
   python merge.py all -l -n output.pdf /path/to/pdfs /path/to/destination
   ```

2. **Selectively merge specific PDFs**:
   ```bash
   python merge.py select -i file1.pdf file2.pdf -a -d /path/to/destination -n merged_output.pdf
   ```

## Notification

The script uses `notify-send` for desktop notifications upon successful merging. Ensure it is installed and properly configured on your system.

## Contributing

Feel free to fork the repository and submit pull requests.

## License

Distributed under the MIT License. See `LICENSE` for more information.

---

This README is concise yet comprehensive, giving all necessary instructions for setup and use. Adjust the repository URLs and any specific instructions according to your actual setup or requirements.
