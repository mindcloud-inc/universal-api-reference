# Update Status Page with Instatus

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/:page_id`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Update Status Page](https://instatus.com/help/api/status-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Status page name. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `status` | body | `string` | no | Status page status value, such as UP or HASISSUES. |
| `subdomain` | body | `string` | no | Status page subdomain. |
