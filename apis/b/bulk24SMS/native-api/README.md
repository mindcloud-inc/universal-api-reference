# Bulk24SMS: Native API Reference

A consolidated summary of Bulk24SMS's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.bulk24sms.com/api_doc/home
- **API base URL:** `https://api.bulk24sms.com/api`

## Authentication

### Auth Key

Authenticate Bulk24SMS public API requests with your auth_key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.bulk24sms.com/api_doc/home)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [View Own Profile](actions/view-own-profile.md) | `GET` | [docs](https://api.bulk24sms.com/api_doc/home) |
