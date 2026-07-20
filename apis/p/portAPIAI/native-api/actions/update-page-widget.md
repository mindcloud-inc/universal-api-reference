# Update Page Widget with Port API AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/pages/:page_identifier/widgets/:widget_id`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Page Widget](https://docs.port.io/api-reference/update-a-widget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint` | body | `string` | yes | Blueprint identifier |
| `blueprintConfig` | body | `object` | yes | Widget blueprint config |
| `dataset` | body | `object` | yes | Widget dataset |
| `page_identifier` | path | `string` | yes | The page identifier. |
| `type` | body | `string` | yes | Widget type |
| `widget_id` | path | `string` | yes | The widget identifier. |
