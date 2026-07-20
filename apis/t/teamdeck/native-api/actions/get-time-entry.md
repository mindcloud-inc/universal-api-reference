# Get Time Entry with Teamdeck

Retrieves a time entry from your Teamdeck organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/time-entries/:id`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Get Time Entry](https://teamdeck.io/developers/api#operation/timeEntryDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Teamdeck time entry ID. |
| `expand` | query | `string` | no | — |
