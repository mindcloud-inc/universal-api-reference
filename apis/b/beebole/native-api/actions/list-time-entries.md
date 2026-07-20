# List Time Entries with Beebole

Retrieves time entries from your Beebole account.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [List Time Entries](https://beebole.com/help/api#list-time-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person.id` | body | `number` | yes | The Beebole person identifier whose time entries should be listed. |
| `from` | body | `string` | yes | The start date for the listing window in YYYY-MM-DD format. |
| `to` | body | `string` | yes | The end date for the listing window in YYYY-MM-DD format. |
