# Generate Report with EARLY

Generates a report in EARLY.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/report`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Generate Report](https://developers.early.app/#04fcb4f6-7a83-4117-91dc-1e9ab75b0519)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date.start` | body | `string` | yes | Report start date in YYYY-MM-DD format. |
| `date.end` | body | `string` | yes | Report end date in YYYY-MM-DD format. |
| `fileType` | body | `string` | yes | Report file type, for example json. |
| `operator` | body | `string` | no | Filter operator, for example OR. |
| `noteQuery` | body | `string` | no | Optional note text filter. |
| `activities.ids` | body | `list<string>` | no | Optional activity ID list. |
| `activities.status` | body | `string` | no | Optional activity status filter. |
| `users.ids` | body | `list<string>` | no | Optional user ID list. |
| `folders.ids` | body | `list<string>` | no | Optional folder ID list. |
| `tags.ids` | body | `list<number>` | no | Optional tag ID list. |
| `mentions.ids` | body | `list<number>` | no | Optional mention ID list. |
