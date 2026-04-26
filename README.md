# veltrix-file-converter

# Veltrix - Premium File Converter

<div align="center">
  
  ![Veltrix Logo](public/favicon.svg)
  
  **A brutalist-inspired, high-performance file conversion tool**
  
  [![Live Demo](https://img.shields.io/badge/demo-live-success)](https://veltrix-file.vercel.app/)
  [![Next.js](https://img.shields.io/badge/Next.js-14-black)](https://nextjs.org/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)](https://www.typescriptlang.org/)
  [![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

  [Live Demo](https://veltrix-file.vercel.app/) · [Report Bug](https://github.com/Shaarim24/veltrix/issues) · [Request Feature](https://github.com/Shaarim24/veltrix/issues)

</div>

---

## 🎯 Overview

Veltrix is a modern, privacy-focused file converter that processes everything locally in your browser and server. No data is sent to third-party services. Built with a striking brutalist design inspired by editorial architecture, it combines aesthetic excellence with powerful functionality.

### ✨ Key Features

- **🔒 Privacy First** - All conversions happen on your server, no third-party APIs
- **⚡ Lightning Fast** - Optimized for 60fps animations and instant conversions
- **🎨 Brutalist Design** - Bold typography, minimal color palette, asymmetric layouts
- **📱 Fully Responsive** - Seamless experience across all devices
- **🖼️ Image Conversion** - JPG, PNG, WebP, GIF support via Sharp
- **🎬 Premium Animations** - GSAP-powered smooth transitions and effects
- **♿ Accessible** - Built with accessibility best practices
- **🚀 Production Ready** - Deployed on Vercel with edge optimization

---

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/Shaarim24/veltrix.git

# Navigate to project directory
cd veltrix

# Install dependencies
npm install

# Run development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the app.

---

## 🛠️ Tech Stack

### Core Framework
- **[Next.js 14](https://nextjs.org/)** - React framework with App Router
- **[TypeScript](https://www.typescriptlang.org/)** - Type-safe development
- **[React 18](https://react.dev/)** - UI library

### File Processing
- **[Sharp](https://sharp.pixelplumbing.com/)** - High-performance image processing
- **[file-type](https://github.com/sindresorhus/file-type)** - File type detection
- **[Multer](https://github.com/expressjs/multer)** - File upload handling

### Animation & Design
- **[GSAP](https://greensock.com/gsap/)** - Professional-grade animations
- **[Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk)** - Modern geometric font
- **Custom CSS** - Brutalist design system

### Deployment
- **[Vercel](https://vercel.com/)** - Edge deployment platform

---

## 📁 Project Structure

```
veltrix/
├── app/
│   ├── api/
│   │   └── convert/
│   │       └── route.ts          # File conversion API endpoint
│   ├── globals.css               # Global styles & brutalist design
│   ├── layout.tsx                # Root layout with metadata
│   └── page.tsx                  # Main page component
├── components/
│   ├── lanterne/
│   │   ├── HeroLanterne.tsx      # Hero section with animations
│   │   ├── FeatureGrid.tsx       # Feature showcase
│   │   ├── ImageGrid.tsx         # Visual gallery
│   │   ├── TextSection.tsx       # Content sections
│   │   └── FinalCTA.tsx          # Call-to-action & footer
│   ├── LanterneExperience.tsx    # Main experience orchestrator
│   └── ...                       # Other components
├── public/
│   ├── favicon.svg               # Site favicon
│   └── icon.svg                  # App icon
└── package.json
```

---

## 🎨 Design Philosophy

Veltrix embraces **brutalist design principles** inspired by [Lanterne Architectes](https://lanterne-architectes.com/):

- **Bold Typography** - Space Grotesk font at large scales
- **Limited Color Palette** - Beige (#f5e6dc) background, red (#d63031) accents, black text
- **Asymmetric Layouts** - Dynamic, editorial-style compositions
- **Minimal Decoration** - Focus on content and functionality
- **Raw Materials** - Exposed structure, honest design

---

## 🔧 How It Works

### File Conversion Flow

1. **Upload** - User selects a file (drag & drop or click)
2. **Detection** - File type is automatically detected using magic bytes
3. **Processing** - File is converted server-side using Sharp (images) or appropriate library
4. **Download** - Converted file is returned with proper MIME type and filename

### Supported Formats

#### Images (via Sharp)
- **Input**: JPG, PNG, WebP, GIF, BMP, TIFF
- **Output**: JPG, PNG, WebP, GIF

#### Future Support
- Audio: MP3, WAV, OGG (via FFmpeg)
- Video: MP4, WebM, AVI (via FFmpeg)
- Documents: PDF, TXT (via pdf-lib)

---

## ⚡ Performance Optimizations

- **GPU Acceleration** - `translateZ(0)` and `backface-visibility: hidden`
- **CSS Containment** - Isolated rendering contexts
- **RAF Throttling** - Smooth 60fps animations
- **Lazy Loading** - Components load on demand
- **Image Optimization** - Next.js automatic image optimization
- **Edge Functions** - Fast global response times

---

## 🚀 Deployment

### Deploy to Vercel (Recommended)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/Shaarim24/veltrix)

Or manually:

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

### Environment Variables

No environment variables required! Veltrix works out of the box.

---

## 📝 API Reference

### POST `/api/convert`

Convert a file to a different format.

**Request:**
```typescript
FormData {
  file: File        // File to convert
  format: string    // Target format (e.g., 'png', 'jpg', 'webp')
}
```

**Response:**
```typescript
// Success: Binary file data with headers
Content-Type: image/png
Content-Disposition: attachment; filename="converted.png"

// Error: JSON
{
  error: string
}
```

**Limits:**
- Max file size: 50MB
- Supported formats: See "Supported Formats" section

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Shaarim Alam**

- Portfolio: [shaarim.vercel.app](https://shaarim.vercel.app)
- GitHub: [@Shaarim24](https://github.com/Shaarim24)

---

## 🙏 Acknowledgments

- Design inspiration from [Lanterne Architectes](https://lanterne-architectes.com/)
- [GSAP](https://greensock.com/) for animation capabilities
- [Sharp](https://sharp.pixelplumbing.com/) for image processing
- [Vercel](https://vercel.com/) for hosting

---

## 📊 Project Stats

- **Build Time**: ~45 seconds
- **Bundle Size**: Optimized for production
- **Performance**: 60fps animations, instant conversions
- **Accessibility**: WCAG 2.1 compliant

---

<div align="center">

**[⬆ back to top](#veltrix---premium-file-converter)**

Made with ❤️ by [Shaarim Alam](https://shaarim.vercel.app)

</div>
