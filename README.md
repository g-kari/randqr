# randqr

Random QR Code Generator - A GitHub Pages site that generates and displays random QR codes.

## Features

- **Random QR Code Generation**: Generate multiple QR codes with unique random content
- **Query Parameter Support**: Control the number of QR codes using URL parameters (`?count=10`)
- **Responsive Design**: QR codes automatically resize based on the number generated to prevent them from being too small
- **Unique Content**: Each QR code contains completely unique content to ensure no duplicates
- **Interactive Interface**: Easy-to-use web interface with input controls

## Usage

### Online
Visit the GitHub Pages site: [https://g-kari.github.io/randqr/](https://g-kari.github.io/randqr/)

### Query Parameters
- `count`: Number of QR codes to generate (1-100)
  - Example: `https://g-kari.github.io/randqr/?count=20`

### Local Development
1. Clone the repository
2. Open `index.html` in a web browser
3. Or serve with a local server: `python3 -m http.server 8000`

## How It Works

- **Unique Content Generation**: Each QR code contains unique content including timestamps, random strings, and UUIDs
- **Adaptive Sizing**: QR code size automatically adjusts based on the total number generated:
  - 1-4 codes: 200px
  - 5-9 codes: 150px
  - 10-16 codes: 120px
  - 17-25 codes: 100px
  - 26-36 codes: 80px
  - 37+ codes: 60px
- **Responsive Grid**: Layout automatically adjusts number of columns based on the total count
- **Real-time Generation**: QR codes are generated client-side using the qrcode.js library

## Technical Details

- Pure HTML/CSS/JavaScript - no build process required
- Uses [qrcode.js](https://github.com/soldair/node-qrcode) library for QR code generation
- Responsive design with CSS Grid
- Supports Japanese language interface