# List Calendar Events with Recallai

Retrieves calendar events from Recallai.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/calendar-events/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [List Calendar Events](https://docs.recall.ai/reference/calendar_events_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar_id` | query | `string` | no | Calendar ID |
| `cursor` | query | `string` | no | The pagination cursor value. |
