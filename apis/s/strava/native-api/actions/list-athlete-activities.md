# List Athlete Activities with Strava

Retrieves activities for the authenticated athlete from Strava.

## Endpoint

- **Method:** `GET`
- **Path:** `/athlete/activities`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [List Athlete Activities](https://developers.strava.com/docs/reference/#api-Activities-getLoggedInAthleteActivities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `date` | no | Only return activities that started before this epoch timestamp. |
| `after` | query | `date` | no | Only return activities that started after this epoch timestamp. |
| `per_page` | query | `number` | no | Number of activities to return per page (1-200). |
| `page` | query | `number` | no | Page number to return, starting at 1. |
