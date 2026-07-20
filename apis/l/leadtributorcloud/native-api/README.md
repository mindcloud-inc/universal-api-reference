# leadtributor.cloud: Native API Reference

A consolidated summary of leadtributor.cloud's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://developer.leadtributor.cloud/
- **API base URL:** `https://api.leadtributor.cloud`

## Authentication

### API Key

Use a leadtributor.cloud API key sent as the raw Authorization header value.

### Credentials

- **API Key:** `apiKey` · required · Your leadtributor.cloud API key. Paste only the raw key value, with no Bearer prefix.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://developer.leadtributor.cloud/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Announce Lead Attachment Upload](actions/announce-lead-attachment-upload.md) | `POST /leads/:leadId/attachments` | [docs](https://developer.leadtributor.cloud/) |
| [Commission Lead](actions/commission-lead.md) | `POST /leads/:leadId/commissions` | [docs](https://developer.leadtributor.cloud/) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://developer.leadtributor.cloud/) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:leadId` | [docs](https://developer.leadtributor.cloud/) |
| [List All Lead Notes](actions/list-all-lead-notes.md) | `GET /notes` | [docs](https://developer.leadtributor.cloud/) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://developer.leadtributor.cloud/) |
| [List Lead Notes](actions/list-lead-notes.md) | `GET /leads/:leadId/notes` | [docs](https://developer.leadtributor.cloud/) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://developer.leadtributor.cloud/) |
| [Offer Lead On Market](actions/offer-lead-on-market.md) | `POST /markets/:marketId/brokerages` | [docs](https://developer.leadtributor.cloud/) |
| [Test API Access](actions/test-api-access.md) | `GET /test` | [docs](https://developer.leadtributor.cloud/) |
| [Update Lead](actions/update-lead.md) | `PATCH /leads/:leadId` | [docs](https://developer.leadtributor.cloud/) |
