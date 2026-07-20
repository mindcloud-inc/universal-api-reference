# List Athlete Routes with Strava

Retrieves routes for a Strava athlete.

## Endpoint

- **Method:** `GET`
- **Path:** `/athletes/:id/routes`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [List Athlete Routes](https://developers.strava.com/docs/reference/#api-Routes-getRoutesByAthleteId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the athlete whose routes are requested. |
| `per_page` | query | `number` | no | Number of routes to return per page (1-200). |
| `page` | query | `number` | no | Page number to return, starting at 1. |
