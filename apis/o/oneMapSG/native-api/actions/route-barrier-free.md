# Route (Barrier-Free) with OneMap SG

Retrieves a barrier-free route from OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/bfa/routingsvc/route`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Route (Barrier-Free)](https://www.onemap.gov.sg/apidocs/bfa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | The start location as latitude and longitude. |
| `end` | query | `string` | yes | The destination location as latitude and longitude. |
