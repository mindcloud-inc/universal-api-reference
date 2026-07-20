# List Activity Kudoers with Strava

Retrieves kudoers for a Strava activity.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/:id/kudos`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [List Activity Kudoers](https://developers.strava.com/docs/reference/#api-Activities-getKudoersByActivityId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the activity whose kudoers are requested. |
| `per_page` | query | `number` | no | Number of athletes to return per page (1-200). |
| `page` | query | `number` | no | Page number to return, starting at 1. |
