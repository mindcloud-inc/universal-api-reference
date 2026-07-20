# Update Routing with MRPeasy

Updates an existing routing in MRPeasy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/routings/{{routingId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Update Routing](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routing_id` | path | `number` | yes | MRPeasy routing ID. |
| `title` | body | `string` | no | Updated routing title. |
| `operations` | body | `array<object>` | no | Updated routing operations array. |
