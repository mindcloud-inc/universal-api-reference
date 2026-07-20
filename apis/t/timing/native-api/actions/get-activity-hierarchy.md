# Get Activity Hierarchy with Timing

Retrieves the activity hierarchy from Timing.

## Endpoint

- **Method:** `GET`
- **Path:** `/activity-hierarchy`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [Get Activity Hierarchy](https://web.timingapp.com/docs/#activity-hierarchy-GETapi-v1-activity-hierarchy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start of the activity range. Timing accepts a date or timestamp. |
| `end_date` | query | `string` | yes | End of the activity range. Timing accepts a date or timestamp. |
