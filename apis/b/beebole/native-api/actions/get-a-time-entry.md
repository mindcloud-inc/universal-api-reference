# Get a Time Entry with Beebole

Retrieves a time entry from your Beebole account.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Get a Time Entry](https://beebole.com/help/api#get-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | The Beebole time entry identifier. |
| `date` | body | `string` | yes | The time entry date in YYYY-MM-DD format. |
