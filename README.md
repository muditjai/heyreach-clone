# HeyReach Clone

A full-stack, single-page LinkedIn outreach automation platform clone modeled after HeyReach. Features include Lead Lists & CSV Upload with field mapping, interactive Sequence Builder, automated Sequence Execution Engine, Unibox Message Inbox with simulation triggers, and an 8-KPI Analytics Dashboard.

## Features

- **8-KPI Analytics Dashboard**: Track Connections sent, Messaged leads, InMailed leads, Tagged leads, Accepted connections + %, Replied leads + %, Replied to InMails + %, and Interested leads + %. Includes 7-day activity timeline charts and active campaign progress.
- **Lead Lists & CSV Upload**: Upload CSV lead files with client-side parsing, flexible column mapping (`linkedinUrl`, `firstName`, `lastName`, `jobTitle`, `companyName`, `location`, `email`), and automatic LinkedIn URL deduplication.
- **Sequence Builder & Campaigns**: Build multi-step automation sequences (`VIEW_PROFILE`, `LIKE_POST`, `SEND_CONNECTION_REQUEST`, `WAIT`, `SEND_MESSAGE`, `SEND_INMAIL`) with customizable template variables (`{{firstName}}`, `{{companyName}}`, etc.).
- **Sequence Execution Engine**: Simulates automated sequence steps, interpolating lead variables, checking connection acceptance before messaging, logging real-time analytics events, and automatically halting sequences when a lead replies.
- **Unibox Message Inbox**: Unified 2-pane inbox with `ALL`, `UNREAD`, `FAVORITES` filters, search, message sending, "Interested" lead tagging, and simulation controls for connection acceptances and inbound lead replies.

## Local Development

Run locally without external dependencies:

```bash
node server.js
```

Then open your browser and navigate to: `http://localhost:3000`

For hot-reloading development mode (Node.js v18.11+):

```bash
node --watch server.js
```

## Cloud Run Deployment (GCP)

Deploy directly to Google Cloud Run using `gcloud`:

```bash
gcloud run deploy heyreach-clone --source .
```
