# Track Habit Activity with Lunatask

## Endpoint

- **Method:** `POST`
- **Path:** `/habits/:id/track`
- **Base URL:** `https://api.lunatask.app/v1`
- **Official documentation:** [Track Habit Activity](https://lunatask.app/api/habits-api/track-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the habit |
| `performed_on` | body | `date` | yes | ISO-8601 formatted date when the activity was performed |
