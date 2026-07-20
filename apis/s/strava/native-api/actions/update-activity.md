# Update Activity with Strava

Updates an existing activity in Strava.

## Endpoint

- **Method:** `PUT`
- **Path:** `/activities/:id`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [Update Activity](https://developers.strava.com/docs/reference/#api-Activities-updateActivityById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the activity to update. |
| `name` | body | `string` | no | The new name of the activity. |
| `description` | body | `string` | no | The new description of the activity. |
| `gear_id` | body | `string` | no | The gear identifier to associate with the activity. |
| `trainer` | body | `boolean` | no | Whether the activity was done on a trainer. |
| `commute` | body | `boolean` | no | Whether the activity was a commute. |
