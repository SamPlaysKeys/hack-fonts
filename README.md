# Hack Font Collection

A curated collection of the **Hack typeface** organized for easy installation and deployment across different platforms and environments.

## About Hack

Hack is a typeface designed specifically for source code. It includes monospaced Regular, Bold, Italic, and Bold Italic variants, and was designed with readability in mind. The typeface is based on Bitstream Vera Sans Mono and includes over 1,500 glyphs, providing excellent Unicode coverage.

- **Version**: v3.003
- **Designer**: Christopher Simpkins and contributors
- **License**: MIT License (SIL Open Font License + Bitstream Vera License)
- **Official Repository**: [source-foundry/Hack](https://github.com/source-foundry/Hack)

## Repository Structure

This repository organizes the Hack font family into the following directories:

```
hack-fonts/
├── README.md           # This file
├── LICENSE.md          # Font license information  
├── ATTRIBUTION.md      # Credits and attribution
├── otf/               # OpenType Font files (.otf) [Coming Soon]
├── ttf/               # TrueType Font files (.ttf)
│   ├── Hack-Regular.ttf
│   ├── Hack-Bold.ttf
│   ├── Hack-Italic.ttf
│   └── Hack-BoldItalic.ttf
└── web/               # Web font files and demo
    ├── demo.html          # Font demonstration page
    ├── stylesheet.css     # CSS with @font-face declarations
    ├── hack-regular.woff
    ├── hack-regular.woff2
    ├── hack-bold.woff
    ├── hack-bold.woff2
    ├── hack-italic.woff
    ├── hack-italic.woff2
    ├── hack-bolditalic.woff
    ├── hack-bolditalic.woff2
    ├── hack-*-subset.woff     # Subset versions for web optimization
    └── hack-*-subset.woff2    # Subset versions for web optimization
```

## Installation

### macOS

**System-wide Installation:**
```bash
# Clone the repository to /Library/Fonts
sudo git clone https://github.com/[your-username]/hack-fonts.git /Library/Fonts/hack-fonts

# Or install TTF files directly to system fonts
sudo cp hack-fonts/ttf/*.ttf /Library/Fonts/
```

**User Installation:**
```bash
# Clone to user fonts directory
git clone https://github.com/[your-username]/hack-fonts.git ~/Library/Fonts/hack-fonts

# Or install TTF files to user fonts
cp hack-fonts/ttf/*.ttf ~/Library/Fonts/
```

### Linux

**System-wide Installation:**
```bash
# Clone to system fonts directory
sudo git clone https://github.com/[your-username]/hack-fonts.git /usr/share/fonts/hack-fonts

# Update font cache
sudo fc-cache -f -v

# Or install TTF files directly
sudo mkdir -p /usr/share/fonts/truetype/hack
sudo cp hack-fonts/ttf/*.ttf /usr/share/fonts/truetype/hack/
sudo fc-cache -f -v
```

**User Installation:**
```bash
# Clone to user fonts directory  
mkdir -p ~/.local/share/fonts
git clone https://github.com/[your-username]/hack-fonts.git ~/.local/share/fonts/hack-fonts

# Update user font cache
fc-cache -f -v

# Or install TTF files to user fonts
cp hack-fonts/ttf/*.ttf ~/.local/share/fonts/
fc-cache -f -v
```

### Windows

**Installation via Font Files:**
1. Download or clone this repository
2. Navigate to the `ttf/` directory
3. Select all `.ttf` files
4. Right-click and select "Install" or "Install for all users"

**Installation via PowerShell:**
```powershell
# Download and install (requires PowerShell 5.0+)
git clone https://github.com/[your-username]/hack-fonts.git
Copy-Item "hack-fonts\\ttf\\*.ttf" "$env:SystemRoot\\Fonts\\"
```

## Usage

### Terminal/Code Editors

After installation, you can use Hack in your terminal or code editor:

- **Font Name**: `Hack`
- **Font Family**: `'Hack', monospace`
- **Recommended Size**: 12-14pt for code editing

### Web Development

Include the font in your web projects:

#### Method 1: Link to CSS file
```html
<link rel="stylesheet" href="path/to/hack-fonts/web/stylesheet.css">
```

#### Method 2: Self-host the fonts
```css
@font-face {
  font-family: 'Hack';
  src: url('path/to/hack-regular.woff2') format('woff2'),
       url('path/to/hack-regular.woff') format('woff');
  font-weight: 400;
  font-style: normal;
}

/* Add similar declarations for Bold, Italic, and Bold Italic */
```

#### Method 3: Use in CSS
```css
.code {
  font-family: 'Hack', 'Monaco', 'Consolas', monospace;
  font-size: 14px;
  line-height: 1.5;
}
```

### Available Variants

| Variant | Weight | Style | File Name |
|---------|--------|-------|-----------|
| Regular | 400 | normal | Hack-Regular.ttf |
| Bold | 700 | normal | Hack-Bold.ttf |
| Italic | 400 | italic | Hack-Italic.ttf |
| Bold Italic | 700 | italic | Hack-BoldItalic.ttf |

## Demo

Open `web/demo.html` in your browser to see a comprehensive demonstration of all font variants and character sets.

## License

The Hack typeface is licensed under the MIT License, which includes:
- SIL Open Font License v1.1
- Bitstream Vera License

See [LICENSE.md](LICENSE.md) for full license text.

## Attribution

This repository is a curated collection of the Hack typeface created by:
- **Christopher Simpkins** and contributors
- Based on **Bitstream Vera Sans Mono** by Bitstream, Inc.
- Extended from **DejaVu Sans Mono**

For complete attribution information, see [ATTRIBUTION.md](ATTRIBUTION.md).

## Contributing

This is a font distribution repository. For font improvements or bug reports, please visit the official [Hack repository](https://github.com/source-foundry/Hack).

To contribute to this distribution:
1. Fork this repository
2. Make improvements to the organization, documentation, or build process
3. Submit a pull request

## Links

- **Official Hack Repository**: https://github.com/source-foundry/Hack
- **Hack Website**: https://sourcefoundry.org/hack/
- **Font Specimen**: [web/demo.html](web/demo.html)
- **License**: [LICENSE.md](LICENSE.md)

## Version History

- **v3.003** (2018-03-05): Latest stable release
  - Improved glyph coverage
  - Bug fixes and optimizations
  - Web font optimizations

---

**Quick Install Command for macOS:**
```bash
cd /Library/Fonts && git clone https://github.com/[your-username]/hack-fonts.git
```

**Quick Install Command for Linux:**
```bash  
sudo git clone https://github.com/[your-username]/hack-fonts.git /usr/share/fonts/hack-fonts && sudo fc-cache -f -v
```