# Smartcar: Native API Reference

A consolidated summary of Smartcar's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://smartcar.com/docs/api
- **REST API base URL:** `https://vehicle.api.smartcar.com/v3`
- **REST API base URL:** `https://management.api.smartcar.com/v3`
- **REST API base URL:** `https://compatibility.api.smartcar.com/v3`

## Authentication

### API Authentication

Use Smartcar API credentials to mint an application access token for the v3 API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://iam.smartcar.com/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://smartcar.com/docs/getting-started/how-to/api-authentication)

## Pagination

- **REST API:** Use `page[size]` in the query string to set the page size (default 50; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.
- **REST API:** Use `page[size]` in the query string to set the page size (default 25; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.
- **REST API:** Use `page[size]` in the query string to set the page size (default 25; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compatible Vehicles](actions/compatible-vehicles.md) | `GET https://compatibility.api.smartcar.com/v3/compatible-vehicles` | [docs](https://smartcar.com/docs/api-reference/compatible-vehicles) |
| [Create Subscription](actions/create-subscription.md) | `POST https://management.api.smartcar.com/v3/subscriptions` | [docs](https://smartcar.com/docs/api-reference/create-subscription) |
| [Get Connection](actions/get-connection.md) | `GET /connections/:connectionId` | [docs](https://smartcar.com/docs/api-reference/get-connection) |
| [Get Subscription](actions/get-subscription.md) | `GET https://management.api.smartcar.com/v3/subscriptions/:subscriptionId` | [docs](https://smartcar.com/docs/api-reference/get-subscription) |
| [Get Webhook](actions/get-webhook.md) | `GET https://management.api.smartcar.com/v3/webhooks/:webhookId` | [docs](https://smartcar.com/docs/api-reference/get-webhook) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://smartcar.com/docs/api-reference/list-connections) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET https://management.api.smartcar.com/v3/subscriptions` | [docs](https://smartcar.com/docs/api-reference/list-subscriptions) |
| [List Webhooks](actions/list-webhooks.md) | `GET https://management.api.smartcar.com/v3/webhooks` | [docs](https://smartcar.com/docs/api-reference/list-webhooks) |
| [Remove Connection](actions/remove-connection.md) | `DELETE /connections/:connectionId` | [docs](https://smartcar.com/docs/api-reference/remove-connection) |
| [Remove Subscription](actions/remove-subscription.md) | `DELETE https://management.api.smartcar.com/v3/subscriptions/:subscriptionId` | [docs](https://smartcar.com/docs/api-reference/remove-subscription) |
| [Remove User](actions/remove-user.md) | `DELETE /users/:userId` | [docs](https://smartcar.com/docs/api-reference/remove-user) |
