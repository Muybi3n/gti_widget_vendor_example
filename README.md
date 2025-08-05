# GTI Widget Demo

A demonstration application showcasing Google Threat Intelligence (GTI) widget integration for cybersecurity threat analysis. This tool displays IOC (Indicators of Compromise) data including URLs and file hashes, with real-time threat scoring and detailed threat intelligence reports.

## 🚀 Features

- **IOC Management** - Display and analyze URLs and file hash indicators
- **Real-time Threat Scoring** - Integration with Google Threat Intelligence API for live threat assessments
- **Interactive Widget** - Embedded GTI widget for detailed threat analysis
- **Responsive Design** - Modern, mobile-friendly interface
- **Resizable Panels** - Adjustable widget panel for optimal viewing
- **API Key Management** - Secure storage and verification of GTI API credentials

## 📋 Prerequisites

- Python 3.6+ (for local server)
- Valid Google Threat Intelligence API Key
- Modern web browser with JavaScript enabled

## ⚡ Quick Start

### 1. Setup Local Server

> **Important:** This application must be served over HTTP (not opened as a local file) due to CORS restrictions and API requirements.

#### For Python 3.x:
```bash
# Navigate to the directory containing the HTML file
cd /path/to/your/gti-widget-demo

# Start the server on port 8000
python -m http.server 8000
```

#### For Python 2.x:
```bash
# Navigate to the directory containing the HTML file
cd /path/to/your/gti-widget-demo

# Start the server on port 8000
python -m SimpleHTTPServer 8000
```

### 2. Access the Application

Open your web browser and navigate to:
```
http://localhost:8000
```

If you renamed the HTML file, append the filename:
```
http://localhost:8000/your-filename.html
```

### 3. Configure API Key

1. Click on the **Configuration** section to expand it
2. Enter your Google Threat Intelligence API Key
3. Click **"Verify & Save API Key"**
4. Wait for verification (🟢 green indicator means success)

## 📁 File Structure

```
gti-widget-demo/
├── index.html          # Main application file (rename your HTML file to this)
├── README.md           # This documentation
└── ...                 # Any additional assets
```

## 📖 Usage Instructions

### Initial Setup
1. **Start the local server** as described above
2. **Configure your API key** in the Configuration section
3. **Wait for data enrichment** - threat scores will populate automatically

### Analyzing Threats
1. **Click on any URL or file hash** to open the detailed GTI widget
2. **Click on threat scores** to view comprehensive threat analysis
3. **Use the resize handle** on the left edge of the widget panel to adjust size
4. **Press Escape** or click the overlay to close the widget

### Sample Data
The demo includes sample IOC data:

**URLs:**
- Phishing URLs with various threat levels
- Malicious tracking links
- Suspicious IP addresses with custom ports

**File Hashes (SHA256):**
- Known malware samples
- Suspicious executables
- Various threat classification levels

## 🔗 API Integration

This application integrates with:
- **Google Threat Intelligence API** - for threat scoring and widget display
- **VirusTotal API** - for IOC verification and enrichment

### API Key Requirements
- Valid GTI/VirusTotal API key with appropriate permissions
- Rate limiting applies based on your API tier
- Keys are stored locally in browser localStorage

## 🌐 Browser Compatibility

| Browser | Version |
|---------|---------|
| Chrome  | 60+     |
| Firefox | 60+     |
| Safari  | 12+     |
| Edge    | 79+     |

## 🔒 Security Considerations

- API keys are stored in browser localStorage
- All API communications use HTTPS
- Widget content is sandboxed in iframe
- No sensitive data is transmitted to external servers

## 🐛 Troubleshooting

### Common Issues

**❌ "API Key is invalid" Error:**
- Verify your API key is correct
- Ensure your API key has the necessary permissions
- Check that you have remaining API quota

**❌ Widget Won't Load:**
- Ensure you're accessing via `http://localhost:8000` (not `file://`)
- Check browser console for any JavaScript errors
- Verify API key is properly configured

**❌ CORS Errors:**
- Must use local server (Python HTTP server recommended)
- Cannot open HTML file directly in browser
- Ensure proper HTTP protocol usage

**❌ Styling Issues:**
- Ensure internet connection for Tailwind CSS CDN
- Check that Google Fonts are loading properly

### 🛠️ Development Mode

For development purposes, you can modify the sample data in the JavaScript section:

```javascript
// Modify these arrays in the script section
const urlIocs = [
    { id: "your-url-here", ingest: "1 Hour Ago", first: "1 Day Ago", last: "1 Hour Ago" }
];

const fileIocs = [
    { id: "your-hash-here", ingest: "2 Hours Ago", first: "1 Day Ago", last: "2 Hours Ago" }
];
```

## 🔄 Alternative Server Options

If Python is not available, you can use other local servers:

### Node.js (http-server):
```bash
npm install -g http-server
http-server -p 8000
```

### PHP:
```bash
php -S localhost:8000
```

### Ruby:
```bash
ruby -run -e httpd . -p 8000
```

## 💡 Support

For issues related to:
- **Google Threat Intelligence API** - Consult GTI documentation
- **Application bugs** - Check browser console for error messages
- **Setup issues** - Ensure proper local server configuration

## ⚠️ Important Notes

> **CORS Requirement:** This application **must** be served via HTTP server due to:
> - Modern browser CORS policies blocking `file://` API calls
> - GTI API requiring proper HTTP headers
> - iframe security requiring valid origin validation

> **Demo Purpose:** This application is for demonstration purposes. Always follow your organization's security policies when handling threat intelligence data.

## 📄 License

This is a demonstration application. Ensure compliance with Google Threat Intelligence API terms of service when using with production data.
