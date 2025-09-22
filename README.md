Job Application Tracker Automation
This project automates the tracking of job application emails, parses structured information using a language model, stores it in Google Sheets, and automatically deletes old applications with no response after a month.

Features
Gmail Trigger:
Automatically fetches emails related to job applications using a strong search query.

Email Parsing with LLM:
Uses Gemini Flash 2.5 to extract structured details:
    • Company name
    • Job title
    • Application status (Applied, Pending, Rejected, Interview, Offer, Announcement)
    • Application date
    • Platform (LinkedIn, Naukri, Indeed, Referral, Company Careers Page, etc.)
    • Additional notes (stipend, location, deadline, interview details)

Google Sheets Integration:
Stores parsed job application data.

Automatic Cleanup:
Deletes rows older than 2 months with no response.

Daily Schedule:
Workflow runs automatically every day using n8n Cron node.

Example Output
json
Copy code
{
  "company": "IDFC",
  "jobTitle": "Application Engineer",
  "status": "Applied",
  "date": "2023-10-27",
  "platform": "Company Careers Page",
  "additionalNotes": "Successfully completed pre-screening, next steps pending",
  "threadId": "1996d1cae302a318"
}

