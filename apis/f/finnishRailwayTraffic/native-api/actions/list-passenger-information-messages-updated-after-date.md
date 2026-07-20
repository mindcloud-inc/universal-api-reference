# List passenger information messages updated after date with Finnish Railway Traffic

Retrieves passenger information messages updated after a date in Finnish Railway Traffic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/passenger-information/updated-after/:date`
- **Base URL:** `https://rata.digitraffic.fi`
- **Official documentation:** [List passenger information messages updated after date](https://rata.digitraffic.fi/swagger/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `date` | yes | Departure date used by Digitraffic for the passenger information update lookup. Use ISO date format YYYY-MM-DD. |
