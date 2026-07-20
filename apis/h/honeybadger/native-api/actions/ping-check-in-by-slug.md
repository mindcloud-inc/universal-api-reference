# Ping Check-in by Slug with Honeybadger

Reports a check-in to Honeybadger by slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/check_in/:apiKey/:checkInSlug`
- **Base URL:** `https://api.honeybadger.io/v1`
- **Official documentation:** [Ping Check-in by Slug](https://docs.honeybadger.io/api/reporting-check-ins/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkInSlug` | path | `string` | yes | Slug identifier configured on the Honeybadger check-in. |
