# SpotlightSearch 🔍

A blazingly fast file and application launcher for Windows, inspired by macOS Spotlight. Built with Rust for performance and reliability.

## Features ✨

- **Instant Search**: Lightning-fast file and application search across your Windows system
- **Smart Indexing**: Efficient file indexing with real-time updates
- **Keyboard-First**: Quick activation with customizable hotkeys (default: `Alt + Space`)
- **File Preview**: Quick preview of documents, images, and text files
- **System Actions**: Quickly access system settings and perform actions
- **Rich Results**: See file metadata, locations, and recent usage
- **Customizable**: Adjust search preferences and appearance to your liking

## Installation 📦

### Prerequisites
- Windows 10 or later
- Rust 1.70 or later (for building from source)

### Binary Installation
1. Download the latest release from the [releases page](https://github.com/rhasanm/SpotlightSearch/releases)
2. Run the installer
3. Launch SpotlightSearch using `Alt + Space`

### Building from Source
```bash
# Clone the repository
git clone https://github.com/rhasanm/SpotlightSearch.git
cd SpotlightSearch

# Build the project
cargo build --release

# Run the application
cargo run --release
```

## Usage 🚀

1. Press `Alt + Space` to open the search window
2. Start typing to search for:
   - Applications
   - Files and folders
   - System settings
   - Quick calculations
   - Web bookmarks
3. Use arrow keys to navigate results
4. Press `Enter` to open the selected item
5. Use modifiers for additional actions:
   - `Ctrl + Enter`: Open file location
   - `Shift + Enter`: Copy file path
   - `Alt + Enter`: Show file properties

## Configuration ⚙️

SpotlightSearch can be configured through the settings UI or by editing the `config.toml` file located at:
- Windows: `%APPDATA%\SpotlightSearch\config.toml`

### Sample Configuration
```toml
[general]
hotkey = "Alt + Space"
max_results = 10
theme = "dark"

[indexing]
excluded_folders = [
    "C:\\Windows\\Temp",
    "%APPDATA%\\Local\\Temp"
]
file_types = ["*"]
index_interval = 3600  # seconds
```

## Performance 📊

SpotlightSearch is designed to be lightweight and efficient:
- Memory usage: ~50MB idle
- Instant search results (<50ms)
- Minimal CPU usage during background indexing
- Small disk footprint for index storage

## Contributing 🤝

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Roadmap 🗺️

- [ ] Natural language processing for better search results
- [ ] Plugin system for extensibility
- [ ] Web search integration
- [ ] File content search
- [ ] Multiple language support
- [ ] Cloud sync for settings and custom rules

## Tech Stack 🛠️

- **Rust**: Core application and file system operations
- **windows-rs**: Windows API bindings
- **tokio**: Async runtime
- **tauri**: UI framework
- **SQLite**: Search index storage
- **notify**: File system monitoring

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments 👏

- Inspired by Apple's Spotlight
- Built with Rust and ❤️
- Thanks to all contributors and the Rust community

## Support 💬

- File an [issue](https://github.com/rhasanm/SpotlightSearch/issues)
- Follow updates on [Twitter](https://twitter.com/rhasanm)

---
Made with ❤️ by Pesnik
