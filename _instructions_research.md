# Job Outreach — Step 1: Research

## Goal

Find 5 CEOs, Co-Founders, CTOs, or Owners at tech SaaS startups who
are hiring software developers right now. For each one, research
company info and a recent signal, and save everything to Airtable.
Do not draft any emails in this step.

## Step 1 — Find Leads via Apollo Connector

Search for people using these filters:

- Title: CEO, Co-Founder, CTO, Owner
- Industry: SaaS, B2B Software
- Company employee count: 10–150
- Has email: true
- Currently hiring: true
- Limit: 5 results
- Locations: UK, Germany, Netherlands

Extract per lead:

- First name
- Last name
- Title
- Company name
- Company website
- Email address
- Company country
- Company industry

## Step 2 — Research the Company + Find a Signal

For each lead, find the following:

### Company Info

- What the company does (one sentence max)
- Their main product or service
- Who their customers are (B2B or B2C, what industry)

### Recent Signal

Search for one recent signal in this priority order:

1. Job posting for a developer role in the last 30 days
2. Recent funding round
3. Recent product launch or new feature

Use whichever signal is found first. Only use one signal per lead.
If no company info can be found OR none of the three signals are
found, skip that lead entirely.

## Step 3 — Enrich Email via Apollo

For each lead returned in Step 1, call the Apollo People Enrichment
endpoint using the lead's id to retrieve their email address only.

- Use the lead id from the search results
- Only extract the email address from the enrichment response
- If no email is returned, skip that lead
- Do not enrich any other fields

## Step 4 — Save to Airtable

Using the Airtable connector, save each lead as a new row in:

- Base: Automation Dev Outreach
- Table: Leads

Map fields exactly:

- First Name → first name
- Last Name → last name
- Title → title
- Company → company name
- Website → company website
- Email → email address
- Country → company country
- Industry → company industry
- Company Info → company info
- Recent Signal → signal found
- Status → set to: research

## Rules

- Only save leads where both company info and a signal were found
- If a lead has no email address, skip that lead
- Do not draft any emails
- Do not ask for confirmation, run all steps sequentially
- If Apollo returns fewer than 5 results, use however many come back