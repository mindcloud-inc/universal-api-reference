# Universal API: Native API Reference

A consolidated summary of Universal API's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.universalapi.io/reference/introduction-2
- **API base URL:** `https://api.prod.universalapi.io`

## Authentication

### API Key Token Exchange

Exchange a Universal API API key plus application or consumer ID for a Bearer access token through POST /api/auth.

### Credentials

- **API Key:** `apiKey` · required · Universal API application API key from the Credentials page.
- **Application ID:** `applicationId` · optional · Application ID required when scope is application.
- **Consumer ID:** `consumerId` · optional · Consumer ID required when scope is consumer.
- **Scope:** `scope` · required · Token scope documented by Universal API: application or consumer.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://docs.universalapi.io/reference/auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `meta.next`. The current page number is read from `meta.current`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /api/auth` | [docs](https://docs.universalapi.io/reference/auth) |
| [Create Consumer](actions/create-consumer.md) | `POST /api/consumers` | [docs](https://docs.universalapi.io/reference/create-consumer) |
| [Create Distributor Order](actions/create-distributor-order.md) | `POST /api/distributors/orders` | [docs](https://docs.universalapi.io/reference/create-order) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/webhooks` | [docs](https://docs.universalapi.io/reference/create-webhook) |
| [Delete Consumer](actions/delete-consumer.md) | `DELETE /consumers/{id}` | [docs](https://docs.universalapi.io/reference/delete-consumer) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/webhooks/{id}` | [docs](https://docs.universalapi.io/reference/delete-webhook) |
| [Disable Lost Mode](actions/disable-lost-mode.md) | `POST /api/mdm/devices/{id}/lost-mode/disable` | [docs](https://docs.universalapi.io/reference/disable-lost-mode) |
| [Enable Lost Mode](actions/enable-lost-mode.md) | `POST /api/mdm/devices/{id}/lost-mode/enable` | [docs](https://docs.universalapi.io/reference/enable-lost-mode) |
| [Get APN Certificate](actions/get-apn-certificate.md) | `GET /api/mdm/apn-cert` | [docs](https://docs.universalapi.io/reference/get-apn-cert) |
| [Get Connection](actions/get-connection.md) | `GET /api/connections/{universalApi}/{serviceId}` | [docs](https://docs.universalapi.io/reference/get-connection) |
| [Get Consumer](actions/get-consumer.md) | `GET /api/consumers/{id}` | [docs](https://docs.universalapi.io/reference/consumer-model) |
| [Get Distributor Order](actions/get-distributor-order.md) | `GET /api/distributors/orders/{id}` | [docs](https://docs.universalapi.io/reference/get-order) |
| [Get HRIS Employee](actions/get-hris-employee.md) | `GET /api/hris/employees/{id}` | [docs](https://docs.universalapi.io/reference/get-employee) |
| [Get Product](actions/get-product.md) | `GET /api/distributors/products/{id}` | [docs](https://docs.universalapi.io/reference/get-product) |
| [Get SSO Profile](actions/get-sso-profile.md) | `GET /api/sso/profile` | [docs](https://docs.universalapi.io/reference/get-profile) |
| [List AM Employees](actions/list-am-employees.md) | `GET /api/am/employees` | [docs](https://docs.universalapi.io/reference/list-employees-1) |
| [List AM Orders](actions/list-am-orders.md) | `GET /api/am/orders` | [docs](https://docs.universalapi.io/reference/list-orders) |
| [List Budgets](actions/list-budgets.md) | `GET /api/am/budgets` | [docs](https://docs.universalapi.io/reference/list-budgets) |
| [List Connections](actions/list-connections.md) | `GET /api/connections` | [docs](https://docs.universalapi.io/reference/list-connections) |
| [List Consumers](actions/list-consumers.md) | `GET /api/consumers` | [docs](https://docs.universalapi.io/reference/get-consumer) |
| [List Device Apps](actions/list-device-apps.md) | `GET /api/mdm/devices/{id}/apps` | [docs](https://docs.universalapi.io/reference/list-device-apps) |
| [List Devices](actions/list-devices.md) | `GET /api/mdm/devices` | [docs](https://docs.universalapi.io/reference/list-devices) |
| [List Distributor Orders](actions/list-distributor-orders.md) | `GET /api/distributors/orders` | [docs](https://docs.universalapi.io/reference/list-orders-1) |
| [List Equipment Items](actions/list-equipment-items.md) | `GET /api/am/equipment-items` | [docs](https://docs.universalapi.io/reference/list-equipment-items) |
| [List HRIS Employees](actions/list-hris-employees.md) | `GET /api/hris/employees` | [docs](https://docs.universalapi.io/reference/list-employees) |
| [List Products](actions/list-products.md) | `GET /api/distributors/products` | [docs](https://docs.universalapi.io/reference/list-products) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.universalapi.io/reference/list-webhooks) |
| [Lock Device](actions/lock-device.md) | `POST /api/mdm/devices/{id}/lock` | [docs](https://docs.universalapi.io/reference/lock-device) |
| [SSO Login](actions/sso-login.md) | `GET /api/sso/login` | [docs](https://docs.universalapi.io/reference/login) |
| [Track Shipment](actions/track-shipment.md) | `GET /api/shipment/track/id/{trackingId}/statuses` | [docs](https://docs.universalapi.io/reference/track-shipment) |
