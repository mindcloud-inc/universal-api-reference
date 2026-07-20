# Get Activity with Strava

Retrieves an activity from Strava by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/:id`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [Get Activity](https://developers.strava.com/docs/reference/#api-Activities-getActivityById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the activity to retrieve. |
| `include_all_efforts` | query | `boolean` | no | Whether to include all segment efforts. |
