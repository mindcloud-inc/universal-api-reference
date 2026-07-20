# Get Current Weather Summary with wttr.in

Retrieves the current weather summary from wttr.in.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:location]`
- **Base URL:** `https://wttr.in`
- **Official documentation:** [Get Current Weather Summary](https://github.com/chubin/wttr.in#one-line-output)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | City, airport code, domain, postal code, GPS coordinates, or supported wttr.in location expression. |
