# OptiMonk: Native API Reference

A consolidated summary of OptiMonk's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://support.optimonk.com/en/articles/11874795-optimonk-public-reporting-api
- **OpenAPI specification:** https://api.optimonk.com/documentation/json
- **API base URL:** `https://api.optimonk.com/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required · Paste your OptiMonk Public Reporting API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://support.optimonk.com/en/articles/11874795-optimonk-public-reporting-api)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /account/` | [docs](https://api.optimonk.com/) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/{id}` | [docs](https://api.optimonk.com/) |
| [Get Campaign Report](actions/get-campaign-report.md) | `GET /report/{campaignId}` | [docs](https://api.optimonk.com/) |
| [Get Overall Report](actions/get-overall-report.md) | `GET /report/` | [docs](https://api.optimonk.com/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns/` | [docs](https://api.optimonk.com/) |
| [List Leads](actions/list-leads.md) | `GET /leads/` | [docs](https://api.optimonk.com/) |
