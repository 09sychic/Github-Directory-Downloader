
# 🚀 GitHub Folder Downloader

A sleek, modern web tool that lets you download any GitHub folder as a ZIP file — without cloning the entire repository. Perfect for grabbing specific directories from public or private repos with just a URL.

![GitHub Folder Downloader](https://img.shields.io/badge/GitHub-Folder%20Downloader-8B5CF6?style=for-the-badge&logo=github)

## ✨ Features

- 📁 **Download Any Folder** - Extract specific folders from any GitHub repository
- 🔒 **Private Repository Support** - Use Personal Access Tokens (PAT) for private repos
- ⚡ **Lightning Fast** - Parallel downloads with up to 10 concurrent connections
- 🎨 **Beautiful UI** - Modern, responsive design with dark/light theme support
- 📊 **Real-time Progress** - Live file preview and download progress tracking
- 🔄 **Download History** - Quick access to your recent downloads
- 🛡️ **Secure** - Your PAT is stored locally in your browser, never sent to any server except GitHub's API
- 🎯 **Zero Dependencies** - No installation required, runs entirely in your browser
- 📱 **Mobile Friendly** - Works seamlessly on desktop, tablet, and mobile devices

## 🎯 What Does This Do?

GitHub Folder Downloader solves a common problem: downloading a specific folder from a GitHub repository without cloning the entire repo. This is especially useful when:

- You only need one directory from a large repository
- You want to download a folder from someone else's repository
- You need quick access to specific code examples or resources
- You're working with private repositories and need selective downloads

## 🚀 How to Use

### Basic Usage (Public Repositories)

1. **Paste the GitHub URL** of any folder:
   ```
   https://github.com/owner/repo/tree/main/folder-name
   ```

2. **Click "Download as ZIP"**

3. **Wait for the download** to complete

That's it! Your folder will be downloaded as a ZIP file.

### Advanced Usage (Private Repositories)

1. **Create a Personal Access Token** (PAT):
   - Go to [GitHub Token Settings](https://github.com/settings/tokens/new?scopes=repo&description=GitHub%20Folder%20Downloader)
   - Select the **"repo"** scope for private repository access
   - Generate and copy your token

2. **Expand the "Private Repository Access" section**

3. **Paste your token** in the input field

4. **Click "Test"** to verify your token (optional but recommended)

5. **Enter your GitHub URL** and download as usual

## 🎨 Supported URL Formats

The tool supports various GitHub URL formats:

```
# Specific folder
https://github.com/owner/repo/tree/main/folder-name

# Root directory
https://github.com/owner/repo

# Nested folders
https://github.com/owner/repo/tree/main/path/to/folder

# Different branches
https://github.com/owner/repo/tree/dev/folder-name
```

## ⌨️ Keyboard Shortcuts

- `Cmd/Ctrl + V` - Paste URL
- `Enter` - Start download
- `T` - Toggle theme (dark/light)
- `H` - Show help/expand PAT section

## 🔧 Technical Details

### Technologies Used

- **Pure JavaScript** - No frameworks, just vanilla JS
- **JSZip** - For creating ZIP files in the browser
- **GitHub API** - For fetching repository contents
- **Modern CSS** - With custom properties and animations

### How It Works

1. **URL Parsing** - Extracts owner, repo, branch, and path from the GitHub URL
2. **API Requests** - Uses GitHub's Tree API for fast file listing
3. **Parallel Downloads** - Downloads multiple files simultaneously (10 concurrent)
4. **ZIP Creation** - Compresses files in-browser using JSZip
5. **Browser Download** - Triggers automatic download of the ZIP file

### Performance Optimizations

- **Tree API** - Uses GitHub's Git Tree API for instant file listing (vs recursive directory scanning)
- **Parallel Downloads** - 10 concurrent file downloads for maximum speed
- **Retry Logic** - Automatic retry with exponential backoff for failed requests
- **Rate Limit Handling** - Smart detection and user feedback for API limits

## 🔒 Security & Privacy

- ✅ **No Server** - Everything runs in your browser
- ✅ **Local Storage** - Your PAT is stored locally (never sent to third parties)
- ✅ **Direct API** - Communicates only with GitHub's official API
- ✅ **Open Source** - Full code transparency

## 📋 Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection
- GitHub Personal Access Token (for private repositories only)

## 🎨 Themes

Switch between dark and light themes using the theme toggle button or press `T`.

- **Dark Theme** (Default) - Easy on the eyes for late-night coding
- **Light Theme** - Clean and bright for daytime use

## 📊 Features Breakdown

### File Preview
- Real-time list of files being downloaded
- Status indicators (fetching, done, error)
- File count badge
- Scrollable list for large directories

### Progress Tracking
- Percentage-based progress bar
- Current file count display
- Compression progress
- Failed download counter

### Process Log
- Detailed step-by-step logging
- Error messages and warnings
- File-by-file download tracking
- Scrollable console-style output

### Download History
- Stores last 5 downloads
- One-click reload of previous URLs
- Shows file count and time ago
- Persistent across sessions

## 🐛 Troubleshooting

### "Repository not found. If private, add a PAT."
- The repository is private. Add a Personal Access Token with "repo" scope.

### "Authentication failed. Check your PAT."
- Your token is invalid or expired. Generate a new one.
- Make sure your token has the "repo" scope enabled.

### "Rate limit exceeded. Add a PAT for more requests."
- GitHub limits anonymous API requests. Add a PAT for higher limits (5,000 requests/hour).

### "No files found in the specified folder"
- Double-check your URL is correct
- Ensure the folder exists in the specified branch
- Try accessing the folder directly on GitHub to verify

## 🤝 Contributing

Contributions are welcome! Feel free to:

- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📝 License

This project is open source and available under the MIT License.

## 👤 Author

Created by [@09sychic](https://github.com/09sychic)

## 🌟 Star This Repo

If you find this tool useful, please consider giving it a star! ⭐

---

**Note**: This tool uses the GitHub API which has rate limits:
- **Without PAT**: 60 requests per hour
- **With PAT**: 5,000 requests per hour

For frequent use or large repositories, we recommend using a Personal Access Token.

## 🔗 Links

- [GitHub Repository](https://github.com/09sychic/github-folder-downloader)
- [Create a Personal Access Token](https://github.com/settings/tokens/new?scopes=repo&description=GitHub%20Folder%20Downloader)
- [GitHub API Documentation](https://docs.github.com/en/rest)

---

by [@09sychic](https://github.com/09sychic)
