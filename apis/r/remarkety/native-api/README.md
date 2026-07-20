# Remarkety: Native API Reference

A consolidated summary of Remarkety's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://support.remarkety.com/hc/en-us/articles/115005328223-Remarkety-Custom-API-V2
- **API base URL:** `https://app.remarkety.com`

## Authentication

### API Key

Remarkety custom API key authentication for server-side REST API access.

### Credentials

- **API Key:** `apiKey` · required
- **Store ID:** `storeId` · required · Store ID from Settings > API Keys in Remarkety.

Send these headers with each API request:

```http
x-api-key: <apiKey>
X-Token: <apiKey>
```

[Official authentication documentation](https://support.remarkety.com/hc/en-us/articles/360044121611-Unsubscribing-a-contact-using-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Upsert Contacts](actions/batch-upsert-contacts.md) | `POST /api/v2/stores/{{credentials.storeId}}/contacts/batch` | [docs](https://support.remarkety.com/hc/en-us/articles/360000694746-Uploading-contacts-in-batch-via-API) |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | `POST /api/v1/stores/{{credentials.storeId}}/contacts/unsubscribe` | [docs](https://support.remarkety.com/hc/en-us/articles/360044121611-Unsubscribing-a-contact-using-API) |
| [Upsert Contact](actions/upsert-contact.md) | `POST /api/v1/stores/{{credentials.storeId}}/contacts` | [docs](https://support.remarkety.com/hc/en-us/articles/115000520263-Sending-contact-information-via-API) |
