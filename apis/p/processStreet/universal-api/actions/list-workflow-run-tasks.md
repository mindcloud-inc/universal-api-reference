# Process Street: List Workflow Run Tasks



```
GET https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-workflow-run-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-workflow-run-tasks?connectionId=$CONNECTION_ID&workflowRunId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowRunId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-workflow-run-tasks?${params}`, {
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
| `workflowRunId` | string | yes | The ID of the workflow run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hidden": true,
      "id": "string",
      "links": [
        {}
      ],
      "name": "Ava Chen",
      "status": "string",
      "stopped": true,
      "taskType": "string",
      "updatedBy": {},
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "workflowRunId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hidden` | boolean |  |
| `id` | string |  |
| `links` | array<object> |  |
| `name` | string |  |
| `status` | string |  |
| `stopped` | boolean |  |
| `taskType` | string |  |
| `updatedBy` | object |  |
| `updatedDate` | date |  |
| `workflowRunId` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `GET /workflow-runs/:workflowRunId/tasks` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-run-tasks.md) for the provider-specific parameters and requirements.

