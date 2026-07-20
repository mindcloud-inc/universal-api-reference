# Change Duration with Clockodo

Updates the clock duration in your Clockodo account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/clock/:id`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Change Duration](https://www.clockodo.com/en/api/clock/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Clockodo running entry ID. |
| `duration_before` | body | `number` | yes | Original duration in seconds. |
| `duration` | body | `number` | yes | New duration in seconds. |
