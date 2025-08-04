Your_Product_Detections - GTI Widget Demo
This project is a self-contained HTML file that demonstrates the integration of the Google Threat Intelligence (GTI) widget into a simulated Security Information and Event Management (SIEM) dashboard. It's designed to provide a realistic and interactive demo for customers, showcasing how GTI can enrich security data directly within a familiar interface.

The entire application is built within a single acme_siem_dashboard.html file, requiring no backend or build steps to run.

Features
Realistic SIEM Interface: A clean, modern dashboard layout displaying URL and file hash matches.

Dynamic GTI Score Enrichment: On page load, the dashboard automatically fetches the GTI threat score for each indicator using the provided API key.

Color-Coded Threat Scores: Scores are color-coded based on severity (Red for high, Orange for medium, Green for low) for at-a-glance threat assessment.

Interactive Slider Widget: Clicking on an indicator or its score opens a sleek, resizable slider panel from the right side of the screen, displaying the full, detailed GTI report in an iframe.

Secure API Key Handling: A collapsible configuration panel allows users to enter their GTI API key. The key is verified against the VirusTotal API, and its status is shown with a clear color-coded indicator (red, orange, green). The key is saved securely in the browser's localStorage.

Resizable Widget Panel: The slider panel containing the GTI widget can be dynamically resized by dragging its left edge to suit the user's preference.

Self-Contained & Portable: The entire demo is a single HTML file with no external dependencies beyond Tailwind CSS loaded from a CDN.

How to Use
Open the File: Launch the acme_siem_dashboard.html file in any modern web browser.

Enter API Key:

Click on the Configuration section at the top to expand it.

Enter your valid Google Threat Intelligence API key into the input field.

Verify & Save:

Click the "Verify & Save API Key" button.

The application will make a test call to the API. The status indicator in the configuration header will turn:

Orange while verifying.

Green upon successful verification and saving.

Red if the key is invalid.

Once the key is verified, the GTI scores for all indicators in the tables will be automatically fetched and displayed.

View a Report:

Click on any indicator link (the URL or file hash) or its corresponding GTI score badge.

The GTI widget will slide out from the right, displaying the full intelligence report for that indicator.

Resize the Widget:

Hover over the left edge of the slider panel until the cursor changes.

Click and drag to resize the panel to your desired width.

Close the Widget:

Click the "×" button in the top-right corner of the slider.

Click on the faded overlay covering the main content.

Press the Escape key.
