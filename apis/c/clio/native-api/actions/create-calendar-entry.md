# Create Calendar Entry with Clio Manage

Creates a new calendar entry in Clio Manage.

## Endpoint

- **Method:** `POST`
- **Path:** `/calendar_entries.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Create Calendar Entry](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Calendar%20Entries/operation/CalendarEntry%23create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.summary` | body | `string` | yes | Short summary of the calendar entry. |
| `data.start_at` | body | `string` | yes | Calendar entry start timestamp in ISO-8601 format. |
| `data.end_at` | body | `string` | yes | Calendar entry end timestamp in ISO-8601 format. |
| `data.calendar_owner.id` | body | `number` | yes | Calendar that owns the calendar entry. |
| `data.description` | body | `string` | no | Detailed description of the calendar entry. |
