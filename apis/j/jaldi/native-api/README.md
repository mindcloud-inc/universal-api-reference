# Jaldi: Native API Reference

A consolidated summary of Jaldi's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://jalditech.com/support/
- **API base URL:** `https://api.jalditech.com`

## Authentication

### API Key

Use the Jaldi campaign API key shown on the campaign details page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://jalditech.com/support/sending-leads-to-jaldi-via-webhooks-connect-to-website-lead-forms/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | `POST /add_on/webhook/add` | [docs](https://jalditech.com/support/sending-leads-to-jaldi-via-webhooks-connect-to-website-lead-forms/) |
| [List Leads](actions/list-leads.md) | `POST /add_on/webhook/fetch_crm_data` | [docs](https://jalditech.com/support/sending-leads-to-jaldi-via-webhooks-connect-to-website-lead-forms/) |
