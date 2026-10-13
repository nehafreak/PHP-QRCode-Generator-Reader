# PHP QR Code Generator and Reader

A PHP library for generating and reading QR codes, based on the implementation by Kazuhiko Arase. The library has been refactored and enhanced with a namespaced structure, flexible output modules, and QR code reading capabilities.

## Features

- Generate Model 2 QR codes, supporting Versions 1–40.
- Support for error correction levels L, M, Q, and H.
- Support for numeric, alphanumeric, binary, Kanji, and Hanzi encoding modes.
- Generate QR codes in multiple formats, including SVG, HTML, PNG, JPEG, GIF, WebP, JSON, plain text, and EPS.
- Optional PDF output through FPDF.
- Read QR codes using GD or ImageMagick.
- Extend output functionality through flexible output modules.

## Requirements

- PHP 8.4 or later.
- `ext-mbstring` is required.
- `ext-gd` or `ext-imagick` is required for QR code reading.

Optional dependencies include:

- `ext-gd` for GD-based image output.
- `ext-imagick` and ImageMagick for ImageMagick-based output.
- `ext-fileinfo` for QRImagick output.
- `setasign/fpdf` for PDF output.
- `intervention/image` for alternative image output.

## Installation

Install the package using Composer:

```bash
composer require chillerlan/php-qrcode
```

## Quick Start

Generate a QR code from a string or URL using the library's `QRCode` class.

```php
<?php

require_once __DIR__ . '/vendor/autoload.php';

use chillerlan\QRCode\QRCode;

$data = 'https://example.com';

echo '<img src="' . (new QRCode)->render($data) . '" alt="QR Code">';
```

Make sure your PHP environment meets the requirements and that Composer dependencies are installed.

## Documentation

- User Guide: https://php-qrcode.readthedocs.io/
- API Documentation: https://chillerlan.github.io/php-qrcode/
- Original Repository: https://github.com/chillerlan/php-qrcode

## Installation Notes

Use examples from the branch that matches your installed library version. The development branch may contain changes that are incompatible with released versions.

## License

Retain the original project's license and attribution when redistributing or modifying this library. Refer to the original repository for the applicable license terms.
