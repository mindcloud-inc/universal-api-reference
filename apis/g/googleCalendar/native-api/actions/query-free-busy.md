# Query Free/Busy with Google Calendar

Retrieves free/busy information from Google Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `freeBusy`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Query Free/Busy](https://developers.google.com/workspace/calendar/api/v3/reference/freebusy/query)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `timeMin` | body | `date` | yes |
| `timeMax` | body | `date` | yes |
| `items[0].id` | body | `string` | yes |
