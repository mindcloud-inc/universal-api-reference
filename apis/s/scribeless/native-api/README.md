# Scribeless: Native API Reference

A consolidated summary of Scribeless's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.scribeless.co/
- **API base URL:** `https://platform.scribeless.co`

## Authentication

### API Key

Authenticate Scribeless API requests with the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://help.scribeless.co/en/articles/8800702-developers)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | `POST /api/recipients` | [docs](https://docs.scribeless.co/) |
| [Create Recipients](actions/create-recipients.md) | `POST /api/recipients` | [docs](https://docs.scribeless.co/) |
