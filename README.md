# Email Sender Tool

The **Email Sender Tool** is a Node.js-based application that automates the process of sending personalized emails to multiple recipients using an Excel file and a pre-defined HTML email template. This tool is ideal for bulk email campaigns, notifications, or promotional emails.

---

## Features
- Send emails to a list of recipients from an Excel file.
- Use a pre-designed HTML template for professional-looking emails.
- Delay between emails to avoid spam filters.
- Simple and efficient to use.

---

## Prerequisites
Before using this tool, ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- npm (Node.js package manager)

---

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/sagarpanchariyasp/emailSendingTool.git
Navigate to the project directory:
bash
Copy code
cd emailSendingTool
Install dependencies:
bash
Copy code
npm install
Usage
Prepare your emails.xlsx file:

Add a column with all recipient email addresses in the first column of the Excel sheet.
Customize your email template:

Edit the email-template.html file to fit your needs.
Run the application:

bash
Copy code
node email-sender.js
The tool will start sending emails one by one with a 1-minute delay between emails.

File Structure
graphql
Copy code
email-sender-tool/
├── api/                 # (Optional API folder for additional features)
├── node_modules/        # Project dependencies
├── .gitignore           # Files/folders to ignore in Git
├── email-sender.js      # Main script to send emails
├── email-template.html  # HTML template for emails
├── emails.xlsx          # Excel file containing recipient email addresses
├── package.json         # Project metadata and dependencies
├── package-lock.json    # Dependency lock file
How It Works
Excel File Parsing:

The tool reads the email addresses from emails.xlsx using the xlsx library.
Email Template:

The email content is defined in email-template.html.
Email Sending:

The nodemailer library is used to send emails through Gmail's SMTP server.
Delay Mechanism:

A 1-minute delay is added between each email to prevent being flagged as spam.
Dependencies
Nodemailer – For sending emails.
xlsx – For reading and processing Excel files.
Configuration
Update the Gmail account credentials in email-sender.js:

javascript
Copy code
const transporter = nodemailer.createTransport({
  service: 'gmail',
  auth: {
    user: 'your-email@gmail.com',
    pass: 'your-app-password'
  },
});
Use an App Password for better security.
Ensure the file paths for emails.xlsx and email-template.html are correct.

Notes
Ensure your Gmail account has "Less Secure Apps" access enabled or use an App Password.
Avoid sending too many emails in a short period to prevent being flagged by Gmail.
License
This project is licensed under the MIT License. You are free to use, modify, and distribute this project.

Author
Developed by Sagar Panchariya.

Feel free to contribute to the project or report any issues. Happy emailing!

yaml
Copy code

---

### How to Add the README to Your Repository
1. Create a file named `README.md` in the root directory of your project.
2. Paste the content above into the file.
3. Add, commit, and push the README file to GitHub:
   ```bash
   git add README.md
   git commit -m "Add README file"
   git push origin main