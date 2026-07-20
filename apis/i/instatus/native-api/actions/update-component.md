# Update Component with Instatus

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/:page_id/components/:component_id`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Update Component](https://instatus.com/help/api/components)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Component description. |
| `name` | body | `string` | no | Component name. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `status` | body | `string` | no | Component status, such as OPERATIONAL or PARTIALOUTAGE. |
| `component_id` | path | `string` | yes | Instatus component ID. |
