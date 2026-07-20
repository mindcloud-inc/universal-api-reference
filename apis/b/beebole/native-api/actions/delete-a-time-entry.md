# Delete a Time Entry with Beebole

Deletes an existing time entry from Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Delete a Time Entry](https://beebole.com/help/api#delete-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | The Beebole time entry identifier. |
| `date` | body | `string` | yes | The time entry date in YYYY-MM-DD format. |
