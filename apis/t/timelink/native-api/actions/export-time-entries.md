# Export Time Entries with Timelink

Exports time entries from the Timelink workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/timeEntries/export`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Export Time Entries](https://api.timelink.io/documentation#/Time%20Entries/post_api_v1_timeEntries_export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | body | `string` | no | Export start date. |
| `end` | body | `string` | no | Export end date. |
| `client_id` | body | `string` | no | Filter export to one client. |
