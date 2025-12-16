# ChatGPT Panel

A Chrome extension that provides quick access to ChatGPT from any webpage via a side panel.

## Features

- **Side Panel Integration**: Access ChatGPT directly in Chrome's side panel without leaving your current page
- **Quick Text Selection**: Select text on any webpage and press `Cmd+L` (Mac) or `Ctrl+L` (Windows/Linux) to send it to ChatGPT
- **Seamless Experience**: ChatGPT is embedded directly in the side panel for a smooth workflow

## Installation

### From Source

1. Clone this repository:

   ```bash
   git clone https://github.com/tkm5/chatgpt-panel.git
   ```

2. Open Chrome and navigate to `chrome://extensions/`

3. Enable "Developer mode" in the top right corner

4. Click "Load unpacked" and select the `chatgpt-panel` folder

## Usage

### Opening the Side Panel

- Click the extension icon in Chrome's toolbar to open the ChatGPT side panel

### Quick Text Selection (Cmd+L / Ctrl+L)

1. Select any text on a webpage
2. Press `Cmd+L` (Mac) or `Ctrl+L` (Windows/Linux)
3. The side panel will open and the selected text will be automatically inserted into ChatGPT's input field

## Files

```
chatgpt-panel/
├── manifest.json        # Extension configuration
├── background.js        # Service worker for extension events
├── content.js           # Keyboard shortcut detection
├── chatgpt-inject.js    # Injects selected text into ChatGPT
├── sidepanel.html       # Side panel UI
├── sidepanel.css        # Side panel styles
├── sidepanel.js         # Side panel logic
├── config.js            # URL configuration
├── rules.json           # Network request rules
└── icons/
    └── gpt icon.png        # Extension icon
```

## Permissions

- `sidePanel`: Required for side panel functionality
- `storage`: Required to pass selected text between scripts
- `declarativeNetRequest`: Required to enable ChatGPT embedding in iframe
- `host_permissions` for `chatgpt.com`: Required to interact with ChatGPT

## Requirements

- Google Chrome (version 114 or later recommended for Side Panel API)
- An OpenAI account to use ChatGPT
