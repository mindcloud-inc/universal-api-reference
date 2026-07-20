# List Athlete Clubs with Strava

Retrieves clubs for the authenticated athlete from Strava.

## Endpoint

- **Method:** `GET`
- **Path:** `/athlete/clubs`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [List Athlete Clubs](https://developers.strava.com/docs/reference/#api-Clubs-getLoggedInAthleteClubs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `per_page` | query | `number` | no | Number of clubs to return per page (1-200). |
| `page` | query | `number` | no | Page number to return, starting at 1. |
