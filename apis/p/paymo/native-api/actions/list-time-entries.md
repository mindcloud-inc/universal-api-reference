# List Time Entries with Paymo

Retrieves time entries from Paymo.

## Endpoint

- **Method:** `GET`
- **Path:** `entries`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [List Time Entries](https://github.com/paymo-org/api/blob/master/sections/entries.md#getting-time-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `where` | query | `string` | no | Optional raw Paymo filtering expression, for example `task_id=32187742`. |
