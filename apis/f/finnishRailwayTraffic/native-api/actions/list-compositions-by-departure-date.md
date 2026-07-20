# List compositions by departure date with Finnish Railway Traffic

Retrieves train compositions by departure date from Finnish Railway Traffic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/compositions/:departure_date`
- **Base URL:** `https://rata.digitraffic.fi`
- **Official documentation:** [List compositions by departure date](https://rata.digitraffic.fi/swagger/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departure_date` | path | `date` | yes | Train departure date. Use ISO date format YYYY-MM-DD. |
