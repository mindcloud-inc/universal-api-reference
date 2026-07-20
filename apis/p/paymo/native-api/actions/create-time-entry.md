# Create Time Entry with Paymo

Creates a time entry in Paymo.

## Endpoint

- **Method:** `POST`
- **Path:** `entries`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Create Time Entry](https://github.com/paymo-org/api/blob/master/sections/entries.md#creating-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `number` | yes | The Paymo task id. |
| `date` | body | `string` | yes | Entry date in `YYYY-MM-DD` format. Kept as a plain string because Paymo expects a date-only value, not an ISO timestamp. |
| `duration` | body | `number` | yes | Entry duration in seconds. |
| `description` | body | `string` | no | Optional time entry description. |
