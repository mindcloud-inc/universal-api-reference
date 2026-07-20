# Campaign Cleaner: Native API Reference

A consolidated summary of Campaign Cleaner's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.campaigncleaner.com/api-reference/introduction
- **API base URL:** `https://api.campaigncleaner.com`

## Authentication

### API Key

Use your Campaign Cleaner API key from API Management.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-CC-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.campaigncleaner.com/management/api-management)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Campaign](actions/delete-campaign.md) | `POST /v1/delete_campaign` | [docs](https://docs.campaigncleaner.com/api-reference/endpoint/delete-campaign) |
| [Get Campaign](actions/get-campaign.md) | `POST /v1/get_campaign` | [docs](https://docs.campaigncleaner.com/api-reference/endpoint/get-campaign) |
| [Get Campaign PDF Analysis](actions/get-campaign-pdf-analysis.md) | `POST /v1/get_campaign_pdf_analysis` | [docs](https://docs.campaigncleaner.com/api-reference/endpoint/get-campaign-pdf-analysis) |
| [Get Campaign Status](actions/get-campaign-status.md) | `POST /v1/get_campaign_status` | [docs](https://docs.campaigncleaner.com/api-reference/endpoint/get-campaign-status) |
| [Get Credits](actions/get-credits.md) | `GET /v1/get_credits` | [docs](https://docs.campaigncleaner.com/api-reference/endpoint/get-credits) |
| [List Campaigns](actions/list-campaigns.md) | `GET /v1/get_campaign_list` | [docs](https://docs.campaigncleaner.com/api-reference/endpoint/get-campaign-list) |
| [Send Campaign](actions/send-campaign.md) | `POST /v1/send_campaign` | [docs](https://docs.campaigncleaner.com/api-reference/endpoint/send-campaign) |
