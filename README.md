What the project does:
This project scrapes a webpage for information about upcoming music tours and automatically notifies the user via email whenever a new tour event is found. The data for these events is stored in a local SQLite database to avoid repeated notifications for the same event. The script runs periodically, checking for updates and sending an email alert when a new event is detected.

Why the project is useful:
Automated Notifications: Instead of manually checking for new tour events, this project automates the process, ensuring you stay informed about new events without any effort.
Database Storage: By storing past events in a SQLite database, it prevents repeated alerts for the same event.
Email Alerts: With real-time email notifications, you can stay updated on the go, without needing to visit the website frequently.

How users can get started with the project:
1. Clone the repository:
https://github.com/zoro-1906/scraping-tool.git
cd tour-scraper

3. Install dependencies:
You will need Python and the following libraries:
pip install requests selectorlib smtplib

3. Set up the SQLite database:
Create a SQLite database and table if you don't already have it:
CREATE TABLE IF NOT EXISTS events (
    band TEXT,
    city TEXT,
    date TEXT
);

4. Configure the email sender details:
Update the send_email function with your Gmail username and a Gmail app-specific password (not your normal password). You can generate an app password in your Google account's security settings. Make sure to use your own email in both the username and receiver fields.

5. Create the extract.yaml file:
This file should contain the configuration for selectorlib to extract data from the scraped webpage. Refer to the website structure you're scraping to properly configure it.

6. Run the script

7. If you need help or encounter any issues:
Open an issue: Feel free to report bugs or request features on the GitHub issue tracker.
