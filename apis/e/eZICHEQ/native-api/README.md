# EZICHEQ: Native API Reference

A consolidated summary of EZICHEQ's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.ezicheq.com/docs/overview
- **OpenAPI specification:** https://developer.ezicheq.com/assets/api/openapi.json?v=1773875440
- **API base URL:** `https://api.ezicheq.com`

## Authentication

### EZICHEQ OAuth 2.0

EZICHEQ requires an EZICHEQ user to register the app. Authorization Code and Refresh Token are supported, and refresh tokens are one-time use.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://ezicheq.com/api/authorise to approve access.
2. Exchange the returned authorization code with a POST request to https://api.ezicheq.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.ezicheq.com/oauth2/token.

[Official authentication documentation](https://developer.ezicheq.com/docs/overview)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | `POST /item/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Create Label](actions/create-label.md) | `POST /label/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Create Test](actions/create-test.md) | `POST /test` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhook/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Delete Item](actions/delete-item.md) | `DELETE /item/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Delete Label](actions/delete-label.md) | `DELETE /label/v1/:labelNumber` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Delete Test](actions/delete-test.md) | `DELETE /test` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhook/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get Account](actions/get-account.md) | `GET /account/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get Check](actions/get-check.md) | `GET /check/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get Checklist](actions/get-checklist.md) | `GET /checklist/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get Item](actions/get-item.md) | `GET /item/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get Item Type](actions/get-item-type.md) | `GET /item_type/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get Label](actions/get-label.md) | `GET /label/v1/:labelNumber` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get Self Check](actions/get-self-check.md) | `GET /selfcheck/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get User](actions/get-user.md) | `GET /user/v1/:username` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhook/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [List Checklists](actions/list-checklists.md) | `GET /checklist/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [List Checks](actions/list-checks.md) | `GET /check/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [List Item Types](actions/list-item-types.md) | `GET /item_type/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [List Items](actions/list-items.md) | `GET /item/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [List Labels](actions/list-labels.md) | `GET /label/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [List Self Checks](actions/list-self-checks.md) | `GET /selfcheck/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [List Users](actions/list-users.md) | `GET /user/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhook/v1` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Test Connection](actions/test-connection.md) | `GET /test` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Update Item](actions/update-item.md) | `PUT /item/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Update Label](actions/update-label.md) | `PUT /label/v1/:labelNumber` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Update Test](actions/update-test.md) | `PUT /test` | [docs](https://developer.ezicheq.com/docs/endpoints) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhook/v1/:id` | [docs](https://developer.ezicheq.com/docs/endpoints) |
