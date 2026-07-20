# Ubidots: Native API Reference

A consolidated summary of Ubidots's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.ubidots.com/reference
- **API base URL:** `https://industrial.api.ubidots.com/api/v2.0`

## Authentication

### Ubidots Token

Authenticate Ubidots API requests with an account token sent in the X-Auth-Token header.

### Credentials

- **Ubidots Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ubidots.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Export Dashboard Model](actions/export-dashboard-model.md) | `GET /dashboards/:dashboard_key/_/export_models` | [docs](https://docs.ubidots.com/reference/export-dashboard-model) |
| [Get all Dashboards](actions/get-all-dashboards.md) | `GET /dashboards/` | [docs](https://docs.ubidots.com/reference/get-all-dashboards) |
| [Get all Device Groups](actions/get-all-device-groups.md) | `GET /device_groups/` | [docs](https://docs.ubidots.com/reference/get-all-device-groups) |
| [Get all Device Types](actions/get-all-device-types.md) | `GET /device_types/` | [docs](https://docs.ubidots.com/reference/get-all-device-types) |
| [Get all Devices](actions/get-all-devices.md) | `GET /devices/` | [docs](https://docs.ubidots.com/reference/get-all-devices) |
| [Get all Events](actions/get-all-events.md) | `GET /events/` | [docs](https://docs.ubidots.com/reference/get-all-events) |
| [Get all Organizations](actions/get-all-organizations.md) | `GET /organizations/` | [docs](https://docs.ubidots.com/reference/get-all-organizations) |
| [Get all Users](actions/get-all-users.md) | `GET /users/` | [docs](https://docs.ubidots.com/reference/get-all-users) |
| [Get all Variables](actions/get-all-variables.md) | `GET /variables/` | [docs](https://docs.ubidots.com/reference/get-all-variables) |
| [Get Dashboard](actions/get-dashboard.md) | `GET /dashboards/:dashboard_key/` | [docs](https://docs.ubidots.com/reference/get-dashboard) |
| [Get Device](actions/get-device.md) | `GET /devices/:device_key/` | [docs](https://docs.ubidots.com/reference/get-device) |
| [Get Device Group](actions/get-device-group.md) | `GET /device_groups/:device_group_key/` | [docs](https://docs.ubidots.com/reference/get-device-group) |
| [Get Device Last Values](actions/get-device-last-values.md) | `GET /devices/:device_key/_/values/last` | [docs](https://docs.ubidots.com/reference/get-device-last-values) |
| [Get Device Type](actions/get-device-type.md) | `GET /device_types/:device_type_key/` | [docs](https://docs.ubidots.com/reference/get-device-of-device-type) |
| [Get Device Variable](actions/get-device-variable.md) | `GET /devices/:device_key/variables/:variable_key/` | [docs](https://docs.ubidots.com/reference/get-variable) |
| [Get Device Variables](actions/get-device-variables.md) | `GET /devices/:device_key/variables/` | [docs](https://docs.ubidots.com/reference/get-all-variables) |
| [Get Event](actions/get-event.md) | `GET /events/:event_key/` | [docs](https://docs.ubidots.com/reference/get-event) |
| [Get Event Log](actions/get-event-log.md) | `GET /events/:event_key/logs/:log_id/` | [docs](https://docs.ubidots.com/reference/get-event-log) |
| [Get Event Logs](actions/get-event-logs.md) | `GET /events/:event_key/logs/` | [docs](https://docs.ubidots.com/reference/get-event-logs) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organization_key/` | [docs](https://docs.ubidots.com/reference/get-organization) |
| [Get Organization Device](actions/get-organization-device.md) | `GET /organizations/:organization_key/devices/:device_key/` | [docs](https://docs.ubidots.com/reference/get-device-in-organization) |
| [Get Organization Devices](actions/get-organization-devices.md) | `GET /organizations/:organization_key/devices/` | [docs](https://docs.ubidots.com/reference/get-all-devices-of-organization) |
| [Get User](actions/get-user.md) | `GET /users/:user_key/` | [docs](https://docs.ubidots.com/reference/get-user) |
| [Get Variable](actions/get-variable.md) | `GET /variables/:variable_id/` | [docs](https://docs.ubidots.com/reference/get-variable) |
