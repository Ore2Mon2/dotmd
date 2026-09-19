# dotmd
## Markdown Editor

English | [日本語](README.md)

<p align="center">
  <img src="./readme-image/icon-dotmd-arrow.png" width="64" alt="dotmd Icon">
</p>

## Overview
dotmd is a Markdown editor with synchronized three-pane display  
(outline, editor, and preview).
- Real-time preview (edits are reflected instantly)
- Rich Markdown features: Mermaid diagrams, math, code highlighting, and more
- Automatic detection of external file changes
- Multiple-instance support
- Web content fetching
- Visual table editing (with CSV/TSV import)
- draw.io diagram creation and editing
- PDF / HTML / Word file export
- Multi-language UI (Japanese / English)
- Tab mode / Window mode switching (manage multiple files as tabs in one window, or open each in its own window)
- Code-signed distributions (Windows: code signed / macOS: code signed & notarized)

<p align="center">
  <img src="./readme-image/ScreenShot-Mac.png" width="512" alt="ScreenShot">
</p>

---
## Key Features

### 📝 Editor Pane
- **Monaco Editor**: the same editor component used in VS Code
- **Markdown syntax helper**: Ctrl+I opens a picker for Markdown syntax
- **Image insertion**: Ctrl+V pastes images (inserted as HTML)
- **File loading**: drag and drop a .md file to open it
- **Collapsible**: click the title bar to hide (or toggle with Ctrl+D)

### 👁️ Preview Pane
- **Real-time preview**: edits are reflected instantly
- **Mermaid diagrams**: flowcharts, sequence diagrams, and more, rendered automatically
- **Code highlighting**: syntax coloring per language via Prism.js
- **Checklist sync**: checking a box in the preview updates the editor
- **Collapsible**: click the title bar to hide (or toggle with Ctrl+M)
- **Image display**: shows inserted images

### 🗂️ Outline Pane
- **Heading list**: automatically extracts Markdown headings
- **Click to jump**: click a heading to jump to that location
- **Collapsible**: click the title bar to hide (or toggle with Ctrl+L)

### 🔤 Encoding and Line Endings
- **Encoding**: Auto / Shift_JIS / UTF-8 (no BOM) / UTF-8 (with BOM)
  - Auto resolves to UTF-8 (no BOM)
- **Line ending**: Auto / CR+LF / LF
  - Auto resolves to CR+LF on Windows, LF on Mac
- **Status bar**: shows the current file's encoding and line ending
- **Menu access**: [File] → [Encoding] / [Line Ending]

### 📤 Export (PDF / HTML / Word)
- **PDF export**: [File] → Save as PDF (Ctrl+P)
- **HTML export**: [File] → Save as HTML (Ctrl+H)
- **Word export**: [File] → Save as Word (Ctrl+W)
- Exports the preview content as-is, including Mermaid diagrams, math, and code highlighting

### 📥 Web Content Fetching
- **Toolbar button**: click the globe icon to open the URL input dialog
- **Content fetching**: fetches the text content of the page at the given URL
- **Separate window**: shows the fetched content in a read-only editor
- **Copy**: use the "Select All and Copy" button to copy to the clipboard

### 📊 Table Editing
- **Visual editing**: click the icon to launch the table editor in a separate window
- **Icon widget**: an edit icon appears when the cursor is inside a Markdown table
- **CSV/TSV import**: load table data from a file

### 🎨 Diagram Creation and Editing
- **Toolbar button**: click the diagram icon to launch the draw.io editor
- **Diagram creation**: create flowcharts, UML diagrams, network diagrams, and more
- **Auto-save**: saves as `.drawio.svg` and inserts a reference into the Markdown
- **Re-editing**: double-click a diagram in the preview to reopen the editor

### 🌍 Language and Settings
- **Display language**: switch between Japanese and English via [Settings] → [Language]
- **External services**: set your DeepL / Tavily API keys via [Settings] → [External Services Settings...]

### 🌐 Optional Features (require setup)

#### DeepL Translation (Ctrl+T)
- Select text and press Ctrl+T to translate between Japanese and English
- In the editor, the translation replaces the selected text
- In the preview, the translation is shown read-only

#### Tavily Web Search (Ctrl+Q)
- Select text and press Ctrl+Q to show web search results
- Click a result's URL to open it in your browser

---
## Supported Platforms

| Platform | Status | Distribution | Signing |
|----------|--------|---------------|---------|
| **Windows 10/11** | ✅ | Installer / Portable | Code signed |
| **macOS (Apple Silicon)** | ✅ | DMG package | Code signed & notarized |

### Windows

#### Installer
- **File name**: `dotmd_{version}_windows_Setup.exe`
- **Details**:
  - NSIS installer format
  - Creates Desktop / Start Menu shortcuts
  - Config file (config.json) location: `C:\Users\{user}\AppData\Roaming\dotmd\`
  - Code signed

#### Portable
- **File name**: `dotmd_{version}_windows_portable.zip`
- **Details**:
  - No installation needed - just unzip and run
  - Config file lives next to the executable
  - Code signed

### macOS

- **File name**: `dotmd_{version}_macos_arm64.dmg`
- **Supported CPU**: Apple Silicon (M1 / M2 / M3 / M4)
- **Details**:
  - DMG installer
  - Config file (config.json) location: `~/Library/Application Support/dotmd/`
  - Install by dragging into the Applications folder
  - Code signed & notarized (launches without a Gatekeeper warning)

  **Note**: Intel Macs are not supported.

---
## Configuration File

### config.json (created automatically)

Created automatically on first launch.

**Location**:
- **Windows installer build**:
    - config.json location: `C:\Users\{user}\AppData\Roaming\dotmd\`
- **Windows portable build**: same folder as the executable
- **macOS**: `~/Library/Application Support/dotmd/`

---
## Setting Up Optional Features

DeepL, Tavily, and proxy settings are all configured from [Settings] → [External Services Settings...] via tabs.

### DeepL Translation

1. Create an account at [DeepL API](https://www.deepl.com/pro-api) and get an API key (a free plan is available)
2. Open [Settings] → [External Services Settings...], go to the [DeepL] tab, check "Enable" and enter your API key
   - The default API endpoint (`https://api-free.deepl.com`) is fine for the free plan
3. Select text and press Ctrl+T to translate

### Tavily Web Search

1. Create an account at [Tavily](https://tavily.com/) and get an API key (a free plan is available)
2. Open [Settings] → [External Services Settings...], go to the [Tavily] tab, check "Enable" and enter your API key
   - The same tab also lets you set the number of results, search depth (basic/advanced), whether to include a generated answer or raw content, and a query prefix
3. Select text and press Ctrl+Q to search

### Proxy

If you need a proxy (e.g. on a corporate network), configure it in the [Proxy] tab of [Settings] → [External Services Settings...].

- Check "Use proxy"
- Enter your HTTP proxy / HTTPS proxy address (e.g. `http://proxy.example.com:8080`)
- For draw.io diagram editing, **restart the app** for changes to take effect (DeepL / Tavily / web content fetching pick them up as soon as you save)

**Note**: proxy behavior varies by environment and isn't guaranteed to work everywhere.

---
## FAQ

### Q: Does it run on Intel Macs?
A: No. Only Apple Silicon (M1/M2/M3/M4) is supported.

### Q: Can I use it offline?
A: Yes - the core features (editing, preview, saving) work offline. DeepL translation, Tavily search, web content fetching, and the draw.io diagram editor all require an internet connection.

### Q: What does web content fetching actually retrieve?
A: It extracts the body text of the page, with `<script>` and `<style>` tags removed. Images, video, and other media are not fetched.

### Q: Can draw.io diagrams be edited offline?
A: Creating and editing a diagram requires draw.io's online editor (https://embed.diagrams.net/), so an internet connection is needed for that. Once a `.drawio.svg` file has been created, though, it can still be viewed in the preview offline.

---
## Privacy and Security

### Data handling

- **The app connects externally in the following cases**
  - **Version check**: at startup, it fetches release information from GitHub (to notify you of new versions)
  - **Web content fetching**: requests to the URL you enter (only when you use that toolbar feature)
  - **DeepL API**: the text you're translating (only if DeepL is enabled)
  - **Tavily API**: your search query (only if Tavily is enabled)
  - **draw.io editor**: diagram data (communicates with https://embed.diagrams.net/ while creating/editing a diagram)

- Your files, settings, and history are stored **on your own computer**

### Handling of API keys

- DeepL and Tavily API keys are stored in your **local config file** (config.json) and used only to authenticate with each service
- **Do not share your config.json with anyone**

---
## Support / Feedback

- **Issues**: [GitHub Issues](https://github.com/Ore2Mon2/dotmd/issues)

---
## License

© 2026 Ore2Mon2. All rights reserved.

- Copyright to dotmd is owned by the developer (Ore2Mon2). You may not copy, modify, reverse engineer, decompile, disassemble, redistribute, rent, lease, or resell this software without the copyright holder's permission.
- Third-party open-source libraries used internally remain subject to their own respective licenses. See [THIRD-PARTY-LICENSES.md](THIRD-PARTY-LICENSES.md) for details.
- See [LICENSE.md](LICENSE.md) for the full license text.
- The full Terms of Service are available at [https://dotmd.oreno.site/](https://dotmd.oreno.site/).

---
## Disclaimer

This software is provided **"AS IS"**, without warranty of any kind, express or implied, including but not limited to warranties of quality, performance, accuracy, fitness for a particular purpose, and non-infringement of third-party rights.

### Limitation of liability

To the maximum extent permitted by law, the developer is not liable for any damages arising from the use of this software, including but not limited to:

- **Data loss or corruption** (lost files, lost edits, etc.)
- **External API usage charges** (DeepL API, Tavily API fees)
- **Security incidents** (leaked API keys, unauthorized access, etc.)
- **System failures or malfunctions**
- **Any other direct, indirect, incidental, special, punitive, or consequential damages**

### Usage notes

- Keep your API keys (DeepL, Tavily) secure
- Do not share your config.json file with anyone
- External API usage is billed per use - check your usage periodically
- We recommend backing up important files regularly

**Use of this software is entirely at your own risk.**

---
## 📋 Version History

[GitHub Releases](https://github.com/Ore2Mon2/dotmd/releases)
