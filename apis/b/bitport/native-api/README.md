# Bitport: Native API Reference

A consolidated summary of Bitport's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://bitport.io/api
- **API base URL:** `https://api.bitport.io/v2`

## Authentication

### Manual access code

Connect Bitport by creating a Bitport application, generating a one-time access code, and exchanging it for an access token.

### Credentials

- **Application ID:** `applicationId` · required · Your Bitport application ID from the Bitport developer application page.
- **Application Secret:** `applicationSecret` · required · Your Bitport application secret from the Bitport developer application page.
- **Access Code:** `accessCode` · required · http://bitport.io/get-access

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://bitport.io/api)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | `POST /oauth2/access-token` | [docs](https://bitport.io/api) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://bitport.io/api/index.html?url=/v2/me&method=GET) |
