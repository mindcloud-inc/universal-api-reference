# Get Time Zone Details with TimeAPI

Retrieves time zone details by IANA name from TimeAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/timezone/zone`
- **Base URL:** `https://www.timeapi.io`
- **Official documentation:** [Get Time Zone Details](https://www.timeapi.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeZone` | query | `string` | yes | Full IANA time zone name, for example Europe/Amsterdam. |
