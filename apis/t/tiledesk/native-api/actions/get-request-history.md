# Get Request History with Tiledesk

Retrieves message history for a request from Tiledesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/{projectId}/requests/:requestId/history`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Get Request History](https://developer.tiledesk.com/apis/rest-api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | The request identifier. |
