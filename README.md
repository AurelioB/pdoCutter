pdoCutter
=========

A tool to prepare pdf files exported from Pepakura for cutting machines.

Full documentation is on the way. Meanwhile, here are the basics:

## Features

- Creates full PDF files with registration marks which can be printed at once
- While meant for PDFs exported from Pepakura, this should work with any PDF file with vector cutlines
- Take advantage of automatic registration marks reading with Silhouette cutting machines (something not reliable enough in Pepakura viewer for Silhouette Cameo), producing accurate cuts with no manual adjustment nonsense

## TODOs

- Allow users to change general settings:
  - Output folder
  - Path appearance
  - File output options
- Create registration marks directly, making templates optional

## Requirements

- Pepakura Viewer or Designer
- Any decent PDF Printer
- Adobe Illustrator (tested with CC 2014, but should work with CS6)
- Silhouette Connect is not needed, but strongly suggested to take full advantage of the workflow

## Installation

1. Download the [latest release](https://github.com/AurelioB/pdoCutter/releases/latest)
2. Copy the project files into your Adobe Illustrator Scripts preset folder. For example, for Illustrator CC 2014 (english version) these would be the paths:
  - **OSX:** `/Applications/Adobe Illustrator CC 2014/Presets.localized/en_US/Scripts/`
  - **Windows:** `C:\Program Files\Adobe\Adobe Illustrator CC 2014\Presets\en_US\Scripts\`
3. Restart Adobe illustrator
4. Go to `File -> Scripts -> pdoCutter -> pdoCutter`

Alternatively, you can avoid installation and use `File -> Scripts -> Other Script...` to launch `pdoCutter.jsx`directly.

## Usage

2. Configure Pepakura to print vector lines:
  1. Go to `File -> Print and Paper settings`
  2. Activate the `print lines clearly (vector)` option
3. Disable fold lines.
3. Print your model and select the PDF printer
4. Launch **pdoCutter**
5. Select the generated PDF file
6. Select a registration marks template
7. Specify a page range
8. Press start and wait for the process to end. A `silhouette`folder should be created.
9. Print the `silhouette/print.pdf` file
10. If you have Silhouette Connect installed, open the corresponding `silhouette/cut/<page number>.ai`file and send the file to Silhouette Connect as usual.
