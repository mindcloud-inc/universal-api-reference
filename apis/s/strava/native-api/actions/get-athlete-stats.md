# Get Athlete Stats with Strava

Retrieves athlete statistics for a Strava athlete.

## Endpoint

- **Method:** `GET`
- **Path:** `/athletes/:id/stats`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [Get Athlete Stats](https://developers.strava.com/docs/reference/#api-Athletes-getStats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the athlete. |
