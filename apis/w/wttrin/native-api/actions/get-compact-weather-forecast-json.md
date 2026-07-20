# Get Compact Weather Forecast JSON with wttr.in

Retrieves compact weather forecast JSON from wttr.in.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:location]`
- **Base URL:** `https://wttr.in`
- **Official documentation:** [Get Compact Weather Forecast JSON](https://github.com/chubin/wttr.in#json-output)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | City, airport code, domain, postal code, GPS coordinates, or supported wttr.in location expression. |
