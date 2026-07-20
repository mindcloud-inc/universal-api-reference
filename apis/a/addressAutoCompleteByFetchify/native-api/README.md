# Address Auto-Complete by Fetchify: Native API Reference

A consolidated summary of Address Auto-Complete by Fetchify's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.fetchify.com/
- **API base URL:** `https://api.craftyclicks.co.uk/address/1.1`

## Authentication

### Access Token

Use a Fetchify access token from the account's Access Tokens & Statistics page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.fetchify.com/)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Addresses](actions/find-addresses.md) | `GET /find` | [docs](https://docs.fetchify.com/json-api/address-auto-complete.html) |
| [List Supported Countries](actions/list-supported-countries.md) | `GET /countries` | [docs](https://docs.fetchify.com/json-api/address-auto-complete.html) |
| [Retrieve Address](actions/retrieve-address.md) | `GET /retrieve` | [docs](https://docs.fetchify.com/json-api/address-auto-complete.html) |
