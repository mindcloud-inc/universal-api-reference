# Create Lead with Kommo

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Create Lead](https://developers.kommo.com/reference/adding-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `[].name` | body | `string` | no | Lead name |
| `[].price` | body | `number` | no | Lead sale |
| `[].status_id` | body | `number` | no | Stage ID the lead is added to. The first stage of the main pipeline by default. |
| `[].pipeline_id` | body | `number` | no | Pipeline ID the lead is added to. |
| `[].responsible_user_id` | body | `number` | no | Lead responsible user ID. |
| `[].custom_fields_values[]` | body | `array<object>` | no | An array of the current lead custom fields’ values. |
| `[]._embedded` | body | `object` | no | Embedded entities of the lead. |
| `[].tags_to_add[]` | body | `array<object>` | no | Tags attached to the lead. |
