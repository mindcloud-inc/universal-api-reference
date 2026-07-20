# Update Recipients with SignWell

Updates recipients on a sent document in SignWell.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/documents/:id/recipients`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Update Recipients](https://developers.signwell.com/reference/updaterecipients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `recipients[]` | body | `array<object>` | yes | — |
| `recipients[].id` | body | `string` | yes | — |
| `recipients[].name` | body | `string` | yes | Updated name for the recipient. |
| `recipients[].email` | body | `string` | yes | — |
