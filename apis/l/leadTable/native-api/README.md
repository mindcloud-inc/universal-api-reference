# LeadTable: Native API Reference

A consolidated summary of LeadTable's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.lead-table.com/guide/leadtable-docs/getting-started
- **OpenAPI specification:** https://docs.lead-table.com/leadtable-external-api-v3
- **API base URL:** `https://api.lead-table.com/api/v3/external`

## Authentication

### API Key + Email

LeadTable requires two headers on every request: x-api-key and email.

### Credentials

- **API Key:** `apiKey` · required · Your LeadTable API token from Settings > Account.
- **Account Email:** `email` · required · The LeadTable account email shown in the sidebar.

Send these headers with each API request:

```http
email: <email>
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.lead-table.com/guide/leadtable-docs/getting-started)

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Attach webhook](actions/attach-webhook.md) | `POST /attachWebhook` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Check authentication](actions/check-authentication.md) | `GET /auth` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Create campaign](actions/create-campaign.md) | `POST /table/create` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Create customer](actions/create-customer.md) | `POST /customer/create` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Create lead](actions/create-lead.md) | `POST /lead/create` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Detach webhook](actions/detach-webhook.md) | `POST /removeWebhook` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Get lead](actions/get-lead.md) | `GET /lead/{leadID}` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [List campaign leads](actions/list-campaign-leads.md) | `GET /lead/campaign/{campaignID}` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [List customer campaigns](actions/list-customer-campaigns.md) | `GET /campaign/all/{customerID}` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [List customers](actions/list-customers.md) | `GET /customer/all` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Poll webhook event](actions/poll-webhook-event.md) | `GET /pollWebhook/{campaignID}/{topic}` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Search leads by email](actions/search-leads-by-email.md) | `GET /searchLeadByMail/{email}` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Update lead description](actions/update-lead-description.md) | `PUT /lead/{leadID}/description` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Upload lead file](actions/upload-lead-file.md) | `POST /addFile` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
| [Upsert lead field](actions/upsert-lead-field.md) | `PUT /lead/{leadID}` | [docs](https://docs.lead-table.com/leadtable-external-api-v3) |
