# BrowserAct: List Tasks

Retrieves tasks from BrowserAct.

```
GET https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserAct `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Optional BrowserAct task status filter. |
| `workflowId` | string | no | Optional workflow ID filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "credit": 1,
      "finishedAt": "string",
      "id": "string",
      "inputParameters": "string",
      "liveUrl": "https://example.com",
      "profileId": "string",
      "status": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Task creation timestamp. |
| `credit` | number | Credits consumed by the task. |
| `finishedAt` | string | Task finish timestamp when available. |
| `id` | string | Task ID. |
| `inputParameters` | string | Input parameters recorded for the task run. |
| `liveUrl` | string | Live BrowserAct session URL when available. |
| `profileId` | string | Browser profile ID when one exists. |
| `status` | string | Task status. |
| `workflowId` | string | Workflow ID associated with the task. |

## Native endpoint

Through the native BrowserAct API, this operation is `GET /list-tasks` (base URL `https://api.browseract.com/v2/workflow`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

