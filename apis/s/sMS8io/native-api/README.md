# SMS8.io: Native API Reference

A consolidated summary of SMS8.io's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://sms8.io/sms8-api-documentation/
- **API base URL:** `https://app.sms8.io/services`

## Authentication

### API Key

SMS8 uses a query-string API key. The key must be sent as the key parameter on request URLs rather than as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sms8.io/sms8-api-documentation/)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get DLR Status](actions/get-dlr-status.md) | `GET dlr/` | [docs](https://sms8.io/sms8-api-documentation/) |
| [Get Message Status](actions/get-message-status.md) | `GET get-msgs.php` | [docs](https://sms8.io/sms8-api-documentation/) |
| [Send SMS](actions/send-sms.md) | `GET send.php` | [docs](https://sms8.io/sms8-api-documentation/) |
