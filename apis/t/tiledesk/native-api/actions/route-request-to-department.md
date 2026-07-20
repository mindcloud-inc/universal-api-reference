# Route Request To Department with Tiledesk

Routes a request to a department in Tiledesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{projectId}/requests/:requestId/departments`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Route Request To Department](https://developer.tiledesk.com/apis/rest-api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | The request identifier. |
