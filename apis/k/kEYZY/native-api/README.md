# KEYZY: Native API Reference

A consolidated summary of KEYZY's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.keyzy.io/docs/developers/rest-api/general-requirements/
- **API base URL:** `https://api.keyzy.io/v2`

## Authentication

### API Key

Use your KEYZY app_id and api_key to connect.

### Credentials

- **API Key:** `apiKey` · required
- **App ID:** `appId` · required · Your KEYZY app_id.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.keyzy.io/docs/dashboard/app-keys/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud/1.0` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Activation](actions/delete-activation.md) | `DELETE /activations/:id` | [docs](https://www.keyzy.io/docs/developers/rest-api/activations-delete/) |
| [Get Encrypted License File](actions/get-encrypted-license-file.md) | `POST /licenses/encrypted-file` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-encrypted-file/) |
| [Get License](actions/get-license.md) | `GET /licenses/show-license/:serial` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-show-license/) |
| [Get Status Check](actions/get-status-check.md) | `GET /status-check` | [docs](https://www.keyzy.io/docs/developers/rest-api/status-check/) |
| [List Activations](actions/list-activations.md) | `GET /activations/:serial` | [docs](https://www.keyzy.io/docs/developers/rest-api/activations-get/) |
| [List License Products](actions/list-license-products.md) | `POST /licenses/products` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-products/) |
| [List Register Products](actions/list-register-products.md) | `GET /register-products/:serial` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-register-products/) |
| [Register License](actions/register-license.md) | `POST /licenses/register` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-register/) |
| [Update Activation](actions/update-activation.md) | `PUT /activations/:id` | [docs](https://www.keyzy.io/docs/developers/rest-api/activations-put/) |
| [Update License SKU](actions/update-license-sku.md) | `POST /licenses/update-sku` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-update-sku/) |
| [Update License Time](actions/update-license-time.md) | `POST /licenses/update-time` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-update-time/) |
| [Update Register Products](actions/update-register-products.md) | `PUT /register-products/:serial` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-register-products-edit/) |
| [Upgrade License](actions/upgrade-license.md) | `POST /licenses/upgrade` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-upgrade/) |
| [Validate License](actions/validate-license.md) | `POST /licenses/valid` | [docs](https://www.keyzy.io/docs/developers/rest-api/licenses-validate/) |
