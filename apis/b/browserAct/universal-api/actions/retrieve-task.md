# BrowserAct: Retrieve Task

Retrieves a task from BrowserAct.

```
GET https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserAct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-task?${params}`, {
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
| `taskId` | string | yes | Task ID returned by a BrowserAct task run. |

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
      "logDetailUrl": "https://example.com",
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
| `logDetailUrl` | string | Detailed BrowserAct log URL when available. |
| `profileId` | string | Browser profile ID when one exists. |
| `status` | string | Current task status. |
| `workflowId` | string | Workflow ID associated with the task. |

## Native endpoint

Through the native BrowserAct API, this operation is `GET /get-task` (base URL `https://api.browseract.com/v2/workflow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task.md) for the provider-specific parameters and requirements.

