# PDF to Image Converter

This script converts a specific page from a PDF file to a JPEG image.

## Requirements

Make sure you have the following Python packages installed:

- `pdf2image`
- `Pillow`

You can install these packages using pip:

```sh
pip3 install pdf2image pillow
```

Additionally, you need to have poppler-utils installed on your system. You can install it using:

- Debian/Ubuntu:

```sh
sudo apt-get install poppler-utils
```

- macOS (using Homebrew):

```sh
brew install poppler
```

## Installation

Clone this repository:

```sh
git clone https://github.com/haikal-dev/pdf2image.git
cd pdf2image
```

## Usage

To run the script, use the following command:

```sh
./pdf2image <pdf_path> <output_prefix> <page_number>
```

- <pdf_path>: Path to the PDF file.
- <output_prefix>: Prefix for the output image file name.
- <page_number>: Page number to convert to an image (1-based index).

### Example

```sh
./pdf2image example.pdf output 1
```

This will convert the first page of example.pdf to an image named output_page_1.jpg.

## Script Explanation

The script contains a function pdf_to_image which performs the following steps:

1. Converts the specified page of the PDF to an image using the pdf2image library.
2. Saves the resulting image as a JPEG file with the specified prefix and page number.

If the conversion fails (e.g., if the page number is invalid), the script will print an error message and exit.

## License

This project is licensed under the MIT License.

## Acknowledgments

- [pdf2image](https://pypi.org/project/pdf2image/)
- [Pillow](https://pypi.org/project/Pillow/)