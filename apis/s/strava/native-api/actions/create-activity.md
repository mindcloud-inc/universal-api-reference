# Create Activity with Strava

Creates a new activity in Strava.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [Create Activity](https://developers.strava.com/docs/reference/#api-Activities-createActivity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the activity. |
| `sport_type` | body | `string` | yes | The sport type of the activity. |
| `start_date_local` | body | `date` | yes | The local start date/time for the activity. |
| `elapsed_time` | body | `number` | yes | Elapsed time in seconds. |
| `description` | body | `string` | no | Description of the activity. |
| `distance` | body | `number` | no | Distance in meters. |
| `trainer` | body | `boolean` | no | Whether the activity was done on a trainer. |
| `commute` | body | `boolean` | no | Whether the activity was a commute. |
