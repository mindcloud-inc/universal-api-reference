# Get Planning Area by Coordinates with OneMap SG

Retrieves a planning area from OneMap SG by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/popapi/getPlanningarea`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Get Planning Area by Coordinates](https://www.onemap.gov.sg/apidocs/planningarea)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | The latitude to look up the planning area for. |
| `longitude` | query | `number` | yes | The longitude to look up the planning area for. |
| `year` | query | `number` | yes | The reference year for the planning area lookup. |
