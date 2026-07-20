# Move Request To Agent with Tiledesk

Assigns a request to an agent in Tiledesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{projectId}/requests/:requestId/agent`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Move Request To Agent](https://developer.tiledesk.com/apis/rest-api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | The request identifier. |
