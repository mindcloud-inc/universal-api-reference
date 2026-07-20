# ReadyCloud Suite: Native API Reference

A consolidated summary of ReadyCloud Suite's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-00-intro.html
- **API base URL:** `https://www.readycloud.com`

## Authentication

### ReadyCloud OAuth2

OAuth2-style ReadyCloud bearer token auth using a provider app plus scoped bearer and refresh tokens.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.readycloud.com/api/v1/oauth2/authorize to approve access.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `account-read_only wallet_subaccount-read_only backup_config api_client note-read_only backup_config-read_only license_key calendar-read_only order-read_only packaging-read_only account contact-read_only license_key-read_only wallet_subaccount api_client-read_only company-read_only note tracking_number calendar company packaging contact order`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://www.readycloud.com/api/v1/oauth2/token/.

[Official authentication documentation](https://www.readycloud.com/static/api-doc/v2/01-getting-started.html)

### ReadyCloud Bearer Token

Bearer access token for the ReadyCloud API. Generate the token from a ReadyCloud provider app with the documented scope set, then paste it into the connection.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.readycloud.com/static/api-doc/v2/01-getting-started.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `results`.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Box](actions/create-box.md) | `POST /api/v2/orgs/:orgPk/orders/:orderPk/boxes/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-03-boxes.html) |
| [Create Contact](actions/create-contact.md) | `POST /api/v2/orgs/:orgPk/contacts/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-12-contacts.html) |
| [Create Item](actions/create-item.md) | `POST /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/items/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-05-items.html) |
| [Create Note](actions/create-note.md) | `POST /api/v2/orgs/:orgPk/orders/:orderPk/notes/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-07-notes.html) |
| [Create Order](actions/create-order.md) | `POST /api/v2/orgs/:orgPk/orders/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-02-orders.html) |
| [Create Packaging](actions/create-packaging.md) | `POST /api/v2/orgs/:orgPk/packaging/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-09-packaging.html) |
| [Create Product](actions/create-product.md) | `POST /api/v2/orgs/:orgPk/products/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-11-products.html) |
| [Get Box](actions/get-box.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-03-boxes.html) |
| [Get Contact](actions/get-contact.md) | `GET /api/v2/orgs/:orgPk/contacts/:contactPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-12-contacts.html) |
| [Get Item](actions/get-item.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/items/:itemPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-05-items.html) |
| [Get Note](actions/get-note.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/notes/:notePk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-07-notes.html) |
| [Get Order](actions/get-order.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-02-orders.html) |
| [Get Packaging](actions/get-packaging.md) | `GET /api/v2/orgs/:orgPk/packaging/:packagingPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-09-packaging.html) |
| [Get Product](actions/get-product.md) | `GET /api/v2/orgs/:orgPk/products/:productPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-11-products.html) |
| [Get Tracking Detail](actions/get-tracking-detail.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/tracking/:trackingPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-04-tracking.html) |
| [List Boxes](actions/list-boxes.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/boxes/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-03-boxes.html) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v2/orgs/:orgPk/contacts/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-12-contacts.html) |
| [List Items](actions/list-items.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/items/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-05-items.html) |
| [List Notes](actions/list-notes.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/notes/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-07-notes.html) |
| [List Orders](actions/list-orders.md) | `GET /api/v2/orgs/:orgPk/orders/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-02-orders.html) |
| [List Organizations](actions/list-organizations.md) | `GET /api/v2/orgs/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-01-organizations.html) |
| [List Packaging](actions/list-packaging.md) | `GET /api/v2/orgs/:orgPk/packaging/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-09-packaging.html) |
| [List Products](actions/list-products.md) | `GET /api/v2/orgs/:orgPk/products/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-11-products.html) |
| [List Tracking](actions/list-tracking.md) | `GET /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/tracking/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-04-tracking.html) |
| [Update Box](actions/update-box.md) | `PATCH /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-03-boxes.html) |
| [Update Contact](actions/update-contact.md) | `PATCH /api/v2/orgs/:orgPk/contacts/:contactPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-12-contacts.html) |
| [Update Item](actions/update-item.md) | `PATCH /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/items/:itemPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-05-items.html) |
| [Update Note](actions/update-note.md) | `PATCH /api/v2/orgs/:orgPk/orders/:orderPk/notes/:notePk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-07-notes.html) |
| [Update Order](actions/update-order.md) | `PATCH /api/v2/orgs/:orgPk/orders/:orderPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-02-orders.html) |
| [Update Packaging](actions/update-packaging.md) | `PATCH /api/v2/orgs/:orgPk/packaging/:packagingPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-09-packaging.html) |
| [Update Product](actions/update-product.md) | `PATCH /api/v2/orgs/:orgPk/products/:productPk/` | [docs](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-11-products.html) |
