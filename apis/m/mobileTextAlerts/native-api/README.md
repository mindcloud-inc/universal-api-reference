# Mobile Text Alerts: Native API Reference

A consolidated summary of Mobile Text Alerts's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://developers.mobile-text-alerts.com/
- **OpenAPI specification:** https://developers.mobile-text-alerts.com/
- **API base URL:** `https://api.mobile-text-alerts.com/v3`

## Authentication

### API Key

Authenticate with a Mobile Text Alerts API key using a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.mobile-text-alerts.com/getting-started/get-an-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | `POST /subscribers` | [docs](https://developers.mobile-text-alerts.com/api-reference/subscribers#post-subscribers) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/:idOrNumberOrEmail` | [docs](https://developers.mobile-text-alerts.com/api-reference/subscribers#delete-subscribers-idornumberoremail) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:idOrNumberOrEmail` | [docs](https://developers.mobile-text-alerts.com/api-reference/subscribers#get-subscribers-idornumberoremail) |
| [List Deliveries](actions/list-deliveries.md) | `GET /deliveries` | [docs](https://developers.mobile-text-alerts.com/api-reference/deliveries#get-deliveries) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://developers.mobile-text-alerts.com/api-reference/subscribers#get-subscribers) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.mobile-text-alerts.com/api-reference/templates#get-templates) |
| [Send Message](actions/send-message.md) | `POST /send` | [docs](https://developers.mobile-text-alerts.com/api-reference/send#post-send) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /subscribers/:idOrNumberOrEmail` | [docs](https://developers.mobile-text-alerts.com/api-reference/subscribers#patch-subscribers-idornumberoremail) |
| [Verify API Key](actions/verify-api-key.md) | `GET /auth/verify-api-key` | [docs](https://developers.mobile-text-alerts.com/getting-started/get-an-api-key#get-auth-verify-api-key) |
