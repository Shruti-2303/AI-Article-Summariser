# AI Article Summarizer

A Chrome extension that leverages Google's Gemini AI to provide intelligent article summarization directly from your browser. Extract and summarize any article on the web with multiple summary formats including brief, detailed, and bullet-point summaries.

## ✨ Features

- **AI-Powered Summarization**: Uses Google Gemini 2.5 Flash API for high-quality article summaries
- **Multiple Summary Formats**: 
  - Brief Summary (2-3 sentences)
  - Detailed Summary (comprehensive overview)
  - Bullet Points (5-7 key points)
- **One-Click Extraction**: Automatically extracts article content from any webpage
- **Easy Copy**: One-click copy functionality for generated summaries
- **Smart Content Detection**: Intelligently identifies and extracts article text using semantic HTML analysis
- **Secure Storage**: API keys stored securely using Chrome's sync storage
- **Responsive UI**: Clean and intuitive popup interface
- **Error Handling**: Robust error handling with user-friendly messages

## 🚀 Installation

### From Source

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-article-summarizer.git
   cd ai-article-summarizer
   ```

2. **Load the extension in Chrome**
   - Open Chrome and navigate to `chrome://extensions/`
   - Enable "Developer mode" (toggle in the top right)
   - Click "Load unpacked"
   - Select the project directory

3. **Get a Gemini API Key**
   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Create a new API key
   - Copy the API key

4. **Configure the extension**
   - Click on the extension icon in your browser toolbar
   - If prompted, enter your Gemini API key in the options page
   - Or right-click the extension icon → Options to access settings

## 📖 Usage

1. **Navigate to any article** on the web
2. **Click the extension icon** in your Chrome toolbar
3. **Select your preferred summary type**:
   - Brief Summary
   - Detailed Summary
   - Bullet Points
4. **Click "Summarize This Page"**
5. **Wait for the AI to generate** your summary
6. **Copy the summary** using the "Copy Summary" button

## 🛠️ Technologies Used

- **JavaScript** - Core functionality and API integration
- **Chrome Extension API (Manifest V3)** - Extension architecture
- **Google Gemini AI API** - AI-powered summarization
- **HTML/CSS** - User interface
- **Chrome Storage API** - Secure API key storage

## 📁 Project Structure

```
ai-article-summarizer/
├── manifest.json          # Extension configuration
├── popup.html             # Main popup interface
├── popup.js               # Popup logic and API integration
├── content.js             # Content script for article extraction
├── background.js          # Background service worker
├── options.html           # Settings page
├── options.js             # Settings page logic
├── icon.png               # Extension icon
└── README.md              # This file
```

## 🔧 How It Works

1. **Content Extraction**: The content script (`content.js`) runs on web pages and extracts article text by:
   - First looking for semantic `<article>` tags
   - Falling back to extracting all paragraph elements if no article tag is found

2. **Message Passing**: The popup script (`popup.js`) communicates with the content script using Chrome's message passing API to retrieve the extracted text

3. **AI Processing**: The extracted text is sent to Google's Gemini API with a prompt tailored to the selected summary type

4. **Display**: The generated summary is displayed in the popup interface with options to copy

## ⚙️ Configuration

### API Key Setup

The extension requires a Google Gemini API key to function:

1. Get your API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Open the extension options (right-click extension icon → Options)
3. Paste your API key and click "Save Settings"

The API key is stored securely in Chrome's sync storage and is only used to communicate with Google's Gemini API.

## 🎯 Features in Detail

### Summary Types

- **Brief Summary**: Concise 2-3 sentence overview perfect for quick understanding
- **Detailed Summary**: Comprehensive summary covering all main points and key details
- **Bullet Points**: Structured list of 5-7 key insights from the article

### Content Extraction

The extension uses intelligent content detection:
- Prioritizes semantic HTML5 `<article>` elements
- Falls back to paragraph-based extraction for compatibility
- Handles various website structures

## 🐛 Troubleshooting

### "API key not found" error
- Make sure you've entered your Gemini API key in the extension options
- Right-click the extension icon → Options to access settings

### "Could not extract article text" error
- The page might not have extractable content
- Try refreshing the page and trying again
- Some pages with heavy JavaScript might require a page reload

### "Could not establish connection" error
- Reload the extension in `chrome://extensions/`
- Make sure you're on a regular webpage (not chrome:// pages)

## 🔮 Future Improvements

- [ ] Support for multiple AI models
- [ ] Custom summary length options
- [ ] Export summaries to files
- [ ] History of previous summaries
- [ ] Support for PDF summarization
- [ ] Dark mode theme
- [ ] Keyboard shortcuts

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/yourusername/ai-article-summarizer/issues).

## 👤 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/Shruti-2303)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/shruti-sharma-2303)

## 🙏 Acknowledgments

- Google Gemini AI for providing the summarization API
- Chrome Extension documentation for excellent resources

---

⭐ If you find this project helpful, please consider giving it a star!

