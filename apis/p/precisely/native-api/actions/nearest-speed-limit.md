# Nearest Speed Limit with Precisely

Retrieves the nearest speed limit from Precisely by location.

## Endpoint

- **Method:** `GET`
- **Path:** `/streets/v1/speedlimit`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Nearest Speed Limit](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Streets/nearest_speed_limit/nearest_speed_limit.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | Two to five semicolon-separated longitude,latitude coordinate pairs. |
