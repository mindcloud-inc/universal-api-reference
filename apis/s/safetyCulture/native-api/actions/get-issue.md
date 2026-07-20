# Get Issue with SafetyCulture

Retrieves an issue from SafetyCulture.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/v1/incident/{id}`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Get Issue](https://developer.safetyculture.com/reference/incidentsservice_getincidentbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required. The unique ID of the incident to retrieve. Can either be a uuid or a org level unique incident id. Example: IS-4352 |
