# OOPSpam: Native API Reference

A consolidated summary of OOPSpam's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.oopspam.com/docs/
- **API base URL:** `https://api.oopspam.com/v1`

## Authentication

### API Key

Use an OOPSpam dashboard API key or RapidAPI marketplace key to authorize requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.oopspam.com/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Content for Spam](actions/check-content-for-spam.md) | `POST /spamdetection` | [docs](https://www.oopspam.com/docs/#spam-detection) |
| [Check Domain Reputation](actions/check-domain-reputation.md) | `POST /reputation/domain` | [docs](https://www.oopspam.com/docs/#domain-reputation) |
| [Report Misdetection](actions/report-misdetection.md) | `POST /spamdetection/report` | [docs](https://www.oopspam.com/docs/#report) |
