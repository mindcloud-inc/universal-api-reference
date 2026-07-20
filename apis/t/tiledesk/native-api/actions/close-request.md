# Close Request with Tiledesk

Closes a request in the current Tiledesk project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{projectId}/requests/:requestId/close`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Close Request](https://developer.tiledesk.com/apis/rest-api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | The request identifier. |
