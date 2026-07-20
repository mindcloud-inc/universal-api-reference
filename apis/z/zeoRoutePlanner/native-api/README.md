# Zeo Route Planner: Native API Reference

A consolidated summary of Zeo Route Planner's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://api.zeorouteplanner.com/
- **API base URL:** `https://zeorouteplanner.com`

## Authentication

### API Key

Connect Zeo Route Planner with an API key generated from Team Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.zeorouteplanner.com/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Driver](actions/create-driver.md) | `POST /api/v5/drivers` | [docs](https://api.zeorouteplanner.com/create-drivers.html) |
| [Create Pickup Delivery Route](actions/create-pickup-delivery-route.md) | `POST /api/v6/routes` | [docs](https://api.zeorouteplanner.com/pickup-deliver-create-route.html) |
| [Create Route](actions/create-route.md) | `POST /api/v5/routes` | [docs](https://api.zeorouteplanner.com/create-route.html) |
| [Create Stops](actions/create-stops.md) | `POST /api/v5/route_stop` | [docs](https://api.zeorouteplanner.com/create-stops.html) |
| [Delete Driver](actions/delete-driver.md) | `DELETE /api/v5/drivers/:driver_id` | [docs](https://api.zeorouteplanner.com/delete-driver.html) |
| [Delete Pickup Delivery Route](actions/delete-pickup-delivery-route.md) | `DELETE /api/v6/routes/:route_id` | [docs](https://api.zeorouteplanner.com/delete-pickup-delivery-route.html) |
| [Delete Route](actions/delete-route.md) | `DELETE /api/v5/routes/:route_id` | [docs](https://api.zeorouteplanner.com/delete-route.html) |
| [Get Pickup Delivery Route Info](actions/get-pickup-delivery-route-info.md) | `GET /api/v6/routes/:route_id` | [docs](https://api.zeorouteplanner.com/pickup-deliver-get-route-info.html) |
| [Get Pickup Delivery Route Optimized Info](actions/get-pickup-delivery-route-optimized-info.md) | `GET /api/v6/routes/:route_id/optimize_route` | [docs](https://api.zeorouteplanner.com/pickup-delivery-get-route-optimized-info.html) |
| [Get Route Info](actions/get-route-info.md) | `GET /api/v5/routes/:route_id` | [docs](https://api.zeorouteplanner.com/get-route-info.html) |
| [Get Route Optimized Info](actions/get-route-optimized-info.md) | `GET /api/v5/routes/:route_id/optimize_route` | [docs](https://api.zeorouteplanner.com/get-route-optimize-info.html) |
| [List Driver Routes](actions/list-driver-routes.md) | `GET /api/v5/routes` | [docs](https://api.zeorouteplanner.com/get-all-driver-routes.html) |
| [List Drivers](actions/list-drivers.md) | `GET /api/v5/drivers` | [docs](https://api.zeorouteplanner.com/get-all-drivers.html) |
