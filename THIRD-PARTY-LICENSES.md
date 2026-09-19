# Third-Party Licenses

This software uses the following third-party libraries and their respective licenses:

## Application Runtime

### Wails v3
- **License**: MIT License
- **Copyright**: Lea Anthony
- **URL**: https://github.com/wailsapp/wails

### Microsoft Edge WebView2 Runtime (Windows)
- Windows builds render the UI using the WebView2 Runtime, installed separately by Microsoft's WebView2 bootstrapper during setup (not bundled inside this application).
- **License**: Subject to the [Microsoft Edge WebView2 Runtime license terms](https://developer.microsoft.com/microsoft-edge/webview2/), not this project's license
- **URL**: https://developer.microsoft.com/microsoft-edge/webview2/

## Go Backend Dependencies

- **github.com/PuerkitoBio/goquery**: BSD 3-Clause License
- **github.com/Xuanwo/go-locale**: Apache License 2.0
- **github.com/fsnotify/fsnotify**: BSD 3-Clause License
- **github.com/go-ole/go-ole**: MIT License
- **github.com/andybalholm/cascadia**: BSD 2-Clause License
- **github.com/adrg/xdg**: MIT License
- **github.com/godbus/dbus/v5**: BSD 2-Clause License
- **github.com/coder/websocket**: ISC License
- **github.com/gomutex/godocx**: MIT License (Word/.docx export)
- **github.com/jchv/go-winloader**: ISC License
- **github.com/mattn/go-colorable**: MIT License
- **github.com/mattn/go-isatty**: MIT License
- **github.com/srwiley/oksvg**: BSD 3-Clause License - Steven R Wiley (SVG rasterization fallback for Word export)
- **github.com/srwiley/rasterx**: BSD 3-Clause License - Steven R Wiley (rasterization engine used by oksvg)
- **golang.org/x/text**: BSD 3-Clause License (The Go Authors)
- **golang.org/x/net**: BSD 3-Clause License (The Go Authors)
- **golang.org/x/sys**: BSD 3-Clause License (The Go Authors)
- **golang.org/x/image**: BSD 3-Clause License (The Go Authors) (used by oksvg for image decoding)

## Editor & UI Components

- **monaco-editor**: MIT License - Microsoft Corporation

## Markdown Processing

- **markdown-it**: MIT License - Vitaly Puzrin, Alex Kocharin
- **markdown-it-anchor**: MIT License
- **markdown-it-deflist**: MIT License
- **markdown-it-footnote**: MIT License
- **markdown-it-ins**: MIT License
- **markdown-it-katex**: MIT License
- **markdown-it-mark**: MIT License
- **markdown-it-sub**: MIT License
- **markdown-it-sup**: MIT License
- **markdown-it-task-lists**: ISC License

## HTML Sanitization

- **DOMPurify**: Dual-licensed under Apache License 2.0 and Mozilla Public License 2.0 - Cure53 and contributors

## Mathematical & Diagram Rendering

- **katex**: MIT License - Khan Academy
- **mermaid**: MIT License - Knut Sveidqvist

## Syntax Highlighting

- **prismjs**: MIT License - Lea Verou

---

## License Compatibility

This project is distributed under a proprietary license (see [LICENSE.md](LICENSE.md)). All third-party components listed above are licensed under permissive open-source licenses that permit their inclusion in proprietary, closed-source, and commercially distributed software, provided the required copyright and license notices are retained (as listed in this document):

- **MIT / BSD 2-Clause / BSD 3-Clause / ISC License**: Permissive, no copyleft or source-disclosure obligations
- **Apache License 2.0** (go-locale) **/ Mozilla Public License 2.0** (DOMPurify): Permissive, requires preservation of copyright and license notices

## Full License Texts

For complete license texts of each library, please refer to their respective repositories or package registries:

- Go module licenses: see the module's repository (module paths and versions are listed in `go.mod`)
- Frontend library licenses (vendored under `frontend/public/lib/` without their own LICENSE file): check the library's npm page or GitHub repository, e.g. `npm info [package-name] license`
