# SimpliRoute: Native API Reference

A consolidated summary of SimpliRoute's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://documentation.simpliroute.com/
- **API base URL:** `https://api.simpliroute.com`

## Authentication

### API Token

Connect with a SimpliRoute API token from your SimpliRoute account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documentation.simpliroute.com/)

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
| [Create User](actions/create-user.md) | `POST /v1/accounts/drivers/` | [docs](https://documentation.simpliroute.com/) |
| [Create Vehicle](actions/create-vehicle.md) | `POST /v1/routes/vehicles/` | [docs](https://documentation.simpliroute.com/) |
| [Delete User](actions/delete-user.md) | `DELETE /v1/accounts/drivers/:user_id/` | [docs](https://documentation.simpliroute.com/) |
| [Delete Vehicle](actions/delete-vehicle.md) | `DELETE /v1/routes/vehicles/:vehicle_id/` | [docs](https://documentation.simpliroute.com/) |
| [Get Account](actions/get-account.md) | `GET /v1/accounts/me/` | [docs](https://documentation.simpliroute.com/) |
| [Get User](actions/get-user.md) | `GET /v1/accounts/drivers/:user_id/` | [docs](https://documentation.simpliroute.com/) |
| [Get Vehicle](actions/get-vehicle.md) | `GET /v1/routes/vehicles/:vehicle_id/` | [docs](https://documentation.simpliroute.com/) |
| [List Users](actions/list-users.md) | `GET /v1/accounts/drivers/` | [docs](https://documentation.simpliroute.com/) |
| [List Vehicles](actions/list-vehicles.md) | `GET /v1/routes/vehicles/` | [docs](https://documentation.simpliroute.com/) |
| [Update User](actions/update-user.md) | `PUT /v1/accounts/drivers/:user_id/` | [docs](https://documentation.simpliroute.com/) |
| [Update Vehicle](actions/update-vehicle.md) | `PATCH /v1/routes/vehicles/:vehicle_id/` | [docs](https://documentation.simpliroute.com/) |
