# Call Feedback To Airtable

Automation workflow that captures sales call feedback from Close CRM and syncs structured data to Airtable for team analytics and coaching.

## Flow

```
Close CRM (call completed)
  → Webhook trigger
  → Extract call metadata (duration, outcome, notes)
  → Parse feedback fields
  → Push to Airtable
  → Update call statistics
```

## Setup

1. Import `Call Feedback to Airtable.blueprint.json` into your automation platform
2. Configure Close CRM webhook for call completion events
3. Configure Airtable API credentials
4. Map fields as described below

## Airtable Schema

| Column | Type | Description |
|--------|------|-------------|
| SDR Name | Text | Sales rep who made the call |
| Lead Name | Text | Contact called |
| Company | Text | Lead's company |
| Call Duration | Number | Duration in seconds |
| Call Outcome | Select | Connected / Voicemail / No Answer |
| Feedback | Long Text | Rep's notes and feedback |
| Next Steps | Text | Follow-up actions |
| Call Date | Date | When the call was made |
| Quality Score | Number | Self-assessed call quality (1-5) |

## Use Cases

- **Sales coaching** — Review call outcomes and feedback patterns
- **Performance tracking** — Monitor call volume and connection rates
- **Pipeline hygiene** — Ensure follow-ups are logged and actioned
