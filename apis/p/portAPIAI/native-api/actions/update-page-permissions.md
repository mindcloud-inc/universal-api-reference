# Update Page Permissions with Port API AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/pages/:page_identifier/permissions`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Page Permissions](https://docs.port.io/api-reference/update-a-pages-permissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_identifier` | path | `string` | yes | The Port page identifier. |
| `read` | body | `object` | yes | Read permissions object |
| `update` | body | `object` | yes | Update permissions object |
