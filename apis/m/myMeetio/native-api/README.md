# MyMeet.io: Native API Reference

A consolidated summary of MyMeet.io's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://app.mymeet.io/admin/integrations/api/view-documentation
- **API base URL:** `https://app.mymeet.io/api`

## Authentication

### API Key

Bearer token authentication for the MyMeet.io API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.mymeet.io/admin/integrations/api/view-documentation)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | `GET /get-bookings` | [docs](https://app.mymeet.io/admin/integrations/api/view-documentation) |
