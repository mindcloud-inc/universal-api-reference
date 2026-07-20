# Route (Walk, Drive, or Cycle) with OneMap SG

Retrieves a walking, driving, or cycling route from OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/routingsvc/route`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Route (Walk, Drive, or Cycle)](https://www.onemap.gov.sg/apidocs/routing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | The start location as latitude and longitude. |
| `end` | query | `string` | yes | The destination location as latitude and longitude. |
| `routeType` | query | `string` | no | The route type such as walk, drive, or cycle. |
