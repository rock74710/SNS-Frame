# sns-frame

A simple macOS Automator workflow for batch processing images with a fixed white frame, perfect for social media posting. The tool maintains aspect ratios while ensuring consistent border spacing on the long edge.

[English](README.md) | [繁體中文](README_zh_TW.md)

## Purpose

* Batch process images to add a clean white frame
* Maintain original image aspect ratios
* Create a consistent 2048x2048 pixel output with 105px spacing on the long edge
* Perfect for Instagram and other social media platforms that prefer square formats
* Preserve image quality without unwanted cropping

## Requirements

* macOS
* Homebrew
* ImageMagick (`brew install imagemagick`)

## Installation

1. Install ImageMagick using Homebrew:

```bash
brew install imagemagick
```

2. Download the Automator workflow file (`.workflow`)
3. Double-click to install the Quick Action
4. When prompted, click "Install" to add it to your Quick Actions

## How to Use

### Method 1: Using Finder Quick Actions

1. In Finder, select one or multiple images you want to process
2. Right-click on the selected images
3. Navigate to `Services` → `sns-frame` in the context menu
4. Wait for the processing to complete
5. Find the processed images in the same folder with "framed\_" prefix

### Method 2: Using Automator App Directly

1. Open the installed workflow in Automator
2. Click the "Run" button in the top-right corner
3. Select the images you want to process when prompted
4. Wait for the processing to complete

### Method 3: Drag and Drop

1. Open Automator
2. Find sns-frame in your workflows
3. Drag and drop images onto the workflow window
4. Click "Run" to process the images

### Batch Processing Tips

* You can process multiple images at once
* Processing time depends on the number and size of images
* Large batches (100+ images) might take a few minutes
* Progress can be monitored in the Automator window

### Troubleshooting

If you encounter any issues:

1. Ensure ImageMagick is properly installed:

```bash
brew install imagemagick
```

2. Check if the images are in a supported format
3. Verify you have write permissions in the output folder
4. Make sure you have enough disk space

## Output Specifications

* Canvas size: 2048 x 2048 pixels
* Border color: White
* Long edge spacing: 105 pixels from edge
* Format: Same as input file
* Naming convention: "framed\_" + original filename

## Notes

* Original files are preserved
* Images smaller than the target size will not be enlarged
* Works with most common image formats (JPG, PNG, etc.)
