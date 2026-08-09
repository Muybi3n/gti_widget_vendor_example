<div align="center">
  <div>&nbsp;</div>

# GTI Vendor Embed: 3rd-Party Integration Example

[![Proof of Concept](https://img.shields.io/badge/Status-Proof_of_Concept-yellow)](#)
[![Google Threat Intelligence](https://img.shields.io/badge/Integration-GTI-blue)](#)
[![License](https://img.shields.io/badge/license-MIT-green)](#)

</div>

A reference implementation for third-party vendors looking to embed a Google Threat Intelligence (GTI) widget within their own platforms, SaaS products, or security dashboards. It demonstrates the seamless integration of GTI capabilities into external environments without exposing raw API keys or requiring complex backend infrastructure.

> **⚠️ NOTE:** This project is for **Proof of Concept (POC) purposes only**. It is not intended for production use. Do not hardcode sensitive keys or credentials in this repository.

---

## 🚀 Quickstart

```bash
git clone git@github.com:Muybi3n/gti_widget_vendor_example.git
cd gti_widget_vendor_example
```

Configure your environment and run:

```bash
# Embed the widget in your application
# Open the example HTML to see the vendor integration in action
```

## 🏗️ Architecture & Integration

This project is built to be easily adaptable and integrated into existing workflows:

- **Target:** 3rd Party Vendors & SaaS platforms.
- **Pattern:** Embedded iframe / web-component style integration.
- **Security:** Demonstrates secure handling of credentials in vendor spaces.

## 🛡️ Security Best Practices

- **API Keys:** Never hardcode your GTI API keys into the source code.
- **Environment Variables:** Always use environment variables or secure credential vaults to manage access.
- **Scope:** Ensure your API token has only the necessary permissions required for the integration.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Since this is a POC, feel free to fork and adapt it to your specific use cases.
