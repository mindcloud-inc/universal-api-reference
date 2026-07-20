# Delete Time Entry with Trackabi

Deletes an existing time entry from Trackabi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/time-entry/:timeEntryId`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [Delete Time Entry](https://trackabi.com/help/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_entry_id` | path | `number` | yes | The unique ID of the time entry. |
