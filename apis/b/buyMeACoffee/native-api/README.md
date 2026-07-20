# Buy Me a Coffee: Native API Reference

A consolidated summary of Buy Me a Coffee's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developers.buymeacoffee.com/
- **API base URL:** `https://developers.buymeacoffee.com/api/v1`

## Authentication

### Access Token

Use a Buy Me a Coffee personal access token with the documented read-only scope.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.buymeacoffee.com/README.md)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Extra Purchase](actions/get-extra-purchase.md) | `GET /extras/:id` | [docs](https://developers.buymeacoffee.com/apireference.md) |
| [Get Member](actions/get-member.md) | `GET /subscriptions/:id` | [docs](https://developers.buymeacoffee.com/apireference.md) |
| [Get Onetime Supporter](actions/get-onetime-supporter.md) | `GET /supporters/:id` | [docs](https://developers.buymeacoffee.com/apireference.md) |
| [List Extra Purchases](actions/list-extra-purchases.md) | `GET /extras` | [docs](https://developers.buymeacoffee.com/apireference.md) |
| [List Members](actions/list-members.md) | `GET /subscriptions` | [docs](https://developers.buymeacoffee.com/apireference.md) |
| [List Onetime Supporters](actions/list-onetime-supporters.md) | `GET /supporters` | [docs](https://developers.buymeacoffee.com/apireference.md) |
