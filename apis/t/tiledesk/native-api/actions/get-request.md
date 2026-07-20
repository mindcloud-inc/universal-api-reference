# Get Request with Tiledesk

Retrieves a request from the current Tiledesk project.

## Endpoint

- **Method:** `GET`
- **Path:** `/{projectId}/requests/:requestId`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Get Request](https://developer.tiledesk.com/apis/rest-api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | The request identifier. |
