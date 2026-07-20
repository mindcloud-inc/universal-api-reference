# Update Time Entry with Paymo

Updates an existing time entry in Paymo.

## Endpoint

- **Method:** `PUT`
- **Path:** `entries/:entryId`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Update Time Entry](https://github.com/paymo-org/api/blob/master/sections/entries.md#updating-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryId` | path | `number` | yes | The Paymo time entry id. |
| `duration` | body | `number` | no | Updated duration in seconds for date-based entries. |
| `description` | body | `string` | no | Updated time entry description. |
