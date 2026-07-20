# AeroLeads: Native API Reference

A consolidated summary of AeroLeads's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://aeroleads.com/api
- **API base URL:** `https://aeroleads.com`

## Authentication

### API Key

Authenticate AeroLeads requests using an API key from account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.aeroleads.com/en/article/where-is-my-api-key-1sl1p63/)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Company Email](actions/get-company-email.md) | `GET /api/get_email_details` | [docs](https://aeroleads.com/api#email_api_get_started) |
| [Get LinkedIn Details](actions/get-linked-in-details.md) | `GET /api/get_linkedin_details` | [docs](https://aeroleads.com/api#linkedin_api_get_started) |
