# Level: Native API Reference

A consolidated summary of Level's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://levelapi.readme.io/reference/authentication
- **API base URL:** `https://api.level.io/v2`

## Authentication

### API Key

Use a Level API key from Settings -> API keys. Level expects the raw API key in the Authorization header without a Bearer prefix.

### Credentials

- **API Key:** `apiKey` · optional · Your Level API key from Settings -> API keys.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://levelapi.readme.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `starting_after` in the query string as the pagination cursor.

## Filtering

Send filters in the query string.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Devices to Group](actions/assign-devices-to-group.md) | `POST /groups/{id}/devices` | [docs](https://levelapi.readme.io/reference/assigndevicestogroup) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /custom_fields` | [docs](https://levelapi.readme.io/reference/createcustomfield) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://levelapi.readme.io/reference/creategroup) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://levelapi.readme.io/reference/createtag) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /custom_fields/{id}` | [docs](https://levelapi.readme.io/reference/deletecustomfield) |
| [Delete Custom Field Value](actions/delete-custom-field-value.md) | `DELETE /custom_field_values` | [docs](https://levelapi.readme.io/reference/deletecustomfieldvalue) |
| [Delete Device](actions/delete-device.md) | `DELETE /devices/{id}` | [docs](https://levelapi.readme.io/reference/deletedevice) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/{id}` | [docs](https://levelapi.readme.io/reference/deletegroup) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/{id}` | [docs](https://levelapi.readme.io/reference/deletetag) |
| [List Alerts](actions/list-alerts.md) | `GET /alerts` | [docs](https://levelapi.readme.io/reference/listalerts) |
| [List Custom Field Values](actions/list-custom-field-values.md) | `GET /custom_field_values` | [docs](https://levelapi.readme.io/reference/custom-field-values) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom_fields` | [docs](https://levelapi.readme.io/reference/custom-fields) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://levelapi.readme.io/reference/listdevices) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://levelapi.readme.io/reference/listgroups) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://levelapi.readme.io/reference/listtags) |
| [Remove Devices from Group](actions/remove-devices-from-group.md) | `DELETE /groups/{id}/devices` | [docs](https://levelapi.readme.io/reference/removegroupdevices) |
| [Remove Tag from Devices](actions/remove-tag-from-devices.md) | `DELETE /tags/{id}/devices` | [docs](https://levelapi.readme.io/reference/removetagfromdevices) |
| [Resolve Alert](actions/resolve-alert.md) | `POST /alerts/{id}/resolve` | [docs](https://levelapi.readme.io/reference/resolvealert) |
| [Show Alert](actions/show-alert.md) | `GET /alerts/{id}` | [docs](https://levelapi.readme.io/reference/showalert) |
| [Show Custom Field](actions/show-custom-field.md) | `GET /custom_fields/{id}` | [docs](https://levelapi.readme.io/reference/showcustomfield) |
| [Show Device](actions/show-device.md) | `GET /devices/{id}` | [docs](https://levelapi.readme.io/reference/showdevice) |
| [Show Group](actions/show-group.md) | `GET /groups/{id}` | [docs](https://levelapi.readme.io/reference/showgroup) |
| [Show Tag](actions/show-tag.md) | `GET /tags/{id}` | [docs](https://levelapi.readme.io/reference/showtag) |
| [Tag Devices](actions/tag-devices.md) | `POST /tags/{id}/devices` | [docs](https://levelapi.readme.io/reference/tagdevices) |
| [Trigger Webhook](actions/trigger-webhook.md) | `POST /automations/webhooks/{token}` | [docs](https://levelapi.readme.io/reference/triggerwebhook) |
| [Update Custom Field](actions/update-custom-field.md) | `PATCH /custom_fields/{id}` | [docs](https://levelapi.readme.io/reference/updatecustomfield) |
| [Update Custom Field Value](actions/update-custom-field-value.md) | `PATCH /custom_field_values` | [docs](https://levelapi.readme.io/reference/updatecustomfieldvalue) |
| [Update Device](actions/update-device.md) | `PATCH /devices/{id}` | [docs](https://levelapi.readme.io/reference/updatedevice) |
| [Update Group](actions/update-group.md) | `PATCH /groups/{id}` | [docs](https://levelapi.readme.io/reference/updategroup) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/{id}` | [docs](https://levelapi.readme.io/reference/updatetag) |
