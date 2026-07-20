# Record Usage with ChargeOver

Creates a new metered usage record in ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/usage`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Record Usage](https://developer.chargeover.com/docs/api/storing-usage-metered-data/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Optional start date/time for the usage period. |
| `line_item_id` | body | `string` | yes | The subscription line item ID that the usage record belongs to. |
| `to` | body | `string` | no | Optional end date/time for the usage period. |
| `type` | body | `string` | no | Optional usage mode such as add, max, lat, pia, pas, or dlt. |
| `usage_value` | body | `string` | yes | The metered usage value to record. |
