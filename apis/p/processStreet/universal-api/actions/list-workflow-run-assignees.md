# Process Street: List Workflow Run Assignees



```
GET https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-workflow-run-assignees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-workflow-run-assignees?connectionId=$CONNECTION_ID&workflowRunId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowRunId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-workflow-run-assignees?${params}`, {
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
      "email": "ava@example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `GET /workflow-runs/:workflowRunId/assignees` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-run-assignees.md) for the provider-specific parameters and requirements.

