# Job Outreach — Step 2: Draft and Save to Gmail Drafts

## Context

Before drafting any email, read \_about_me.md to understand who is
writing. Read \_voice_guidelines.md for tone and rules. All emails
must reflect both files.

## Goal

Read all rows from Airtable where Status is "approved". For each one,
draft one cold email from Olga's perspective, save to Gmail drafts,
and update the row status to "draft".

## Step 1 — Read Approved Leads from Airtable

Using the Airtable connector, fetch all rows from:

- Base: Automation Dev Outreach
- Table: Leads
- Filter: Status = "approved"

Each row contains:
First Name, Last Name, Title, Company, Website, Email, Company Info,
Recent Signal

## Step 2 — Draft the Email

For each row, draft one cold email following \_voice_guidelines.md
exactly.

Use this as the brief:

---

Writer: Olga Ivanova (see \_about_me.md)
Recipient: {first_name}, {title} at {company_name}
Company context: {company_info}
Signal to reference: {recent_signal}

Write the email body (max 4 sentences) and a subject line (max 8
words) separately. Do not include the subject line in the body.

---

## Step 3 — Save to Drafts via Gmail

Using the Gmail connector, save each email as a draft:

- To: the lead's email address
- Subject: the generated subject line
- Body: the generated email body
- Format: plain text

## Step 4 — Update Airtable

After each draft is saved, update that row in Airtable:

- Status → set to: draft

## Rules

- Only process rows where Status = "approved"
- Do not process rows with any other status
- Save one draft at a time, update Airtable after each one
- Do not ask for confirmation, run all steps sequentially