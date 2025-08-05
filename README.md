# Image Extension Dataset

A comprehensive collection of sample image files in various formats for testing image processing applications, file type detection systems, and format conversion tools.

## Overview

This dataset contains 50+ sample image files representing a wide variety of image formats commonly used in digital imaging, photography, graphics, and web development. The collection includes both common and specialized formats, making it ideal for testing file format detection, image processing libraries, and conversion utilities.

## Dataset Contents

### Image Formats Included

The dataset includes sample files in the following formats:

**Common Web Formats:**
- JPEG (`.jpg`, `.jpeg`, `.jpe`, `.jfif`)
- PNG (`.png`)
- GIF (`.gif`)
- WebP (`.webp`)
- SVG (`.svg`)

**Bitmap Formats:**
- BMP (`.bmp`)
- WBMP (`.wbmp`)
- TGA (`.tga`)
- PCX (`.pcx`)

**Photography/RAW Formats:**
- Canon RAW (`.cr2`)
- Nikon RAW (`.nef`, `.nrw`)
- Olympus RAW (`.orf`)
- Pentax RAW (`.pef`)
- Fuji RAW (`.raf`)
- Panasonic RAW (`.rw2`)
- Sony RAW (`.erf`)
- Adobe DNG (`.dng`)

**High Dynamic Range:**
- HDR (`.hdr`)
- EXR (`.exr`)
- PFM (`.pfm`)

**Specialized Formats:**
- HEIC/HEIF (`.heic`, `.heif`) - Apple's modern image format
- DDS (`.dds`) - DirectDraw Surface for gaming
- PSD (`.psd`) - Adobe Photoshop
- FITS (`.fts`) - Flexible Image Transport System (astronomy)
- JPEG 2000 (`.jp2`)
- JPEG Stereo (`.jps`)
- MNG (`.mng`) - Multiple-image Network Graphics
- PCD (`.pcd`) - Kodak Photo CD

**Icon and Cursor Formats:**
- ICO (`.ico`) - Windows icons
- CUR (`.cur`) - Windows cursors

**Portable Formats:**
- PNM (`.pnm`, `.pam`, `.pbm`, `.pgm`, `.ppm`) - Portable Network formats
- XBM (`.xbm`) - X11 Bitmap
- XPM (`.xpm`) - X11 Pixmap
- XWD (`.xwd`) - X Window Dump

**Legacy and Specialized:**
- PICON (`.picon`) - Personal Icons
- PICT (`.pict`) - Apple QuickDraw
- RAS (`.ras`) - Sun Raster
- SGI (`.sgi`) - SGI Image
- TIFF (`.tiff`) - Tagged Image File Format
- PES (`.pes`) - Embroidery format

### Files Without Extensions

The dataset also includes several test files without file extensions to test format detection based on file headers/magic numbers:

- `jpgnoextension` - JPEG image without extension
- `tifffilenoextension` - TIFF image without extension  
- `xpmnoextension` - XPM image without extension
- `somerandomhash` - BMP image with random filename

## File Structure

```
image-extension-dataset/
├── LICENSE                 # MIT License
├── README.md              # This documentation
└── files/
    ├── files.json         # JSON list of all files
    ├── sample.{ext}       # Sample images with various extensions
    ├── sample-1.{ext}     # Additional samples for some formats
    └── {files-no-ext}     # Test files without extensions
```

## Use Cases

This dataset is particularly useful for:

- **File Type Detection**: Testing libraries that identify file formats based on content rather than extensions
- **Image Processing**: Validating image processing pipelines across multiple formats
- **Format Conversion**: Testing image conversion tools and libraries
- **Web Development**: Testing image upload and processing systems
- **Digital Asset Management**: Testing file organization and metadata extraction tools
- **Computer Vision**: Preprocessing pipelines that need to handle various input formats
- **Quality Assurance**: Testing image viewers, editors, and processing applications

## Technical Details

- **Total Files**: 50+ image files plus metadata
- **File Sizes**: Vary by format and compression
- **Dimensions**: Most sample images are 640x426 pixels (some exceptions for format-specific requirements)
- **Color Depth**: Varies by format capabilities
- **Compression**: Includes both compressed and uncompressed formats

## Usage

### JSON Metadata
The `files/files.json` contains a complete list of all files in the dataset:

```json
{
  "files": [
    "sample.bmp",
    "sample.jpg",
    "sample.png",
    ...
  ]
}
```

### File Type Detection Example
You can use this dataset to test file type detection:

```python
import magic

# Test file type detection
for filename in os.listdir('files/'):
    if filename.endswith(('.json', '.py')):
        continue
    filepath = f'files/{filename}'
    detected_type = magic.from_file(filepath, mime=True)
    print(f"{filename}: {detected_type}")
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

If you have suggestions for additional image formats or improvements to the dataset, please feel free to open an issue or submit a pull request.

## Acknowledgments

This dataset was created to support the development and testing of image processing applications and file format detection systems. Special thanks to the open-source community for the tools and libraries that make working with diverse image formats possible.


## Sources

All images here are not made by me but downloaded somewhere, some of the sources are from the following websites:

* https://filesamples.com/
* https://file-examples.com