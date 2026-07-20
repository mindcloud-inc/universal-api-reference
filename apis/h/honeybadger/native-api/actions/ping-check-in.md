# Ping Check-in with Honeybadger

Reports a check-in to Honeybadger by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/check_in/:checkInId`
- **Base URL:** `https://api.honeybadger.io/v1`
- **Official documentation:** [Ping Check-in](https://docs.honeybadger.io/api/reporting-check-ins/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkInId` | path | `string` | yes | The case-sensitive check-in endpoint ID from Honeybadger. |
