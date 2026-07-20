# Get Current Time By Time Zone with TimeAPI

Retrieves the current time for an IANA time zone from TimeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/time/current/zone`
- **Base URL:** `https://www.timeapi.io`
- **Official documentation:** [Get Current Time By Time Zone](https://www.timeapi.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timezone` | query | `string` | yes | Full IANA time zone name, for example Europe/Amsterdam. |
