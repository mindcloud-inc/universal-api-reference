# Update Destination with Hightouch

Updates an existing destination in Hightouch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/destinations/{destinationId}`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Update Destination](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinationId` | path | `number` | yes | The destination ID. |
| `name` | body | `string` | no | The destination name. |
| `configuration` | body | `object` | no | Destination configuration object for the selected destination type. |
