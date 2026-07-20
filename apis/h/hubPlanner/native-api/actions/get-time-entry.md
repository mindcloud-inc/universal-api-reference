# Get Time Entry with Hub Planner

Retrieves a time entry from Hub Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeentry/:id`
- **Base URL:** `https://api.hubplanner.com/v1`
- **Official documentation:** [Get Time Entry](https://github.com/hubplanner/API/blob/master/Sections/timesheets.md#get-specific-timeentry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hub Planner time entry ID from the _id field. |
