# CardClan: Native API Reference

A consolidated summary of CardClan's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.cardclan.io/api-reference/integration/overview
- **OpenAPI specification:** https://docs.cardclan.io/openapi.json
- **API base URL:** `https://app.cardclan.io/api`

## Authentication

### Integration Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cardclan.io/api-reference/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Integration Configuration](actions/create-integration-configuration.md) | `POST /integration/config` | [docs](https://docs.cardclan.io/api-reference/integration/config/create-config) |
| [Get Card Details](actions/get-card-details.md) | `GET /integration/card-details/:cardId` | [docs](https://docs.cardclan.io/api-reference/integration/overview) |
| [Get Card URL](actions/get-card-url.md) | `POST /integration/get-card-url` | [docs](https://docs.cardclan.io/api-reference/integration/actions/get-card-url) |
| [Get Configuration by Card](actions/get-configuration-by-card.md) | `GET /integration/config/by-card` | [docs](https://docs.cardclan.io/examples/send-card) |
| [Get Integration Configuration](actions/get-integration-configuration.md) | `GET /integration/config` | [docs](https://docs.cardclan.io/api-reference/integration/config/get-config) |
| [List Cards](actions/list-cards.md) | `POST /integration/cards` | [docs](https://docs.cardclan.io/api-reference/integration/data/get-cards) |
| [List Cards With Workflows](actions/list-cards-with-workflows.md) | `GET /integration/workflow-cards` | [docs](https://docs.cardclan.io/api-reference/integration/workflow/workflow-cards) |
| [List Email Accounts](actions/list-email-accounts.md) | `GET /integration/email-accounts` | [docs](https://docs.cardclan.io/api-reference/integration/data/get-email-accounts) |
| [List Workspaces](actions/list-workspaces.md) | `GET /integration/workspaces` | [docs](https://docs.cardclan.io/api-reference/integration/data/get-workspaces) |
| [Send Card](actions/send-card.md) | `POST /integration/send-card` | [docs](https://docs.cardclan.io/api-reference/integration/actions/send-card) |
| [Validate Authentication](actions/validate-authentication.md) | `GET /integration/auth/validate` | [docs](https://docs.cardclan.io/api-reference/integration/authentication/validate-token) |
