# Mailform: Native API Reference

A consolidated summary of Mailform's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.mailform.io/docs/api/
- **API base URL:** `https://www.mailform.io/app/api/v1`

## Authentication

### API Key

Authenticate Mailform API requests with a Bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.mailform.io/docs/api/)

## API conventions

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://www.mailform.io/docs/api/#create-order) |
| [Get All Teams](actions/get-all-teams.md) | `GET /teams` | [docs](https://www.mailform.io/docs/api/#get-all-teams) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://www.mailform.io/docs/api/#get-current-user) |
| [Get Order](actions/get-order.md) | `GET /orders/:order_id` | [docs](https://www.mailform.io/docs/api/#get-order) |
| [Get Rate](actions/get-rate.md) | `POST /rates` | [docs](https://www.mailform.io/docs/api/#get-rate) |
| [Get Team](actions/get-team.md) | `GET /teams/:team_id` | [docs](https://www.mailform.io/docs/api/#get-a-specific-team) |
