# Process Street: List Task Form Field Values



```
GET https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-task-form-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-task-form-field-values?connectionId=$CONNECTION_ID&workflowRunId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowRunId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-task-form-field-values?${params}`, {
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
| `taskId` | string | yes | The ID of the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "fieldType": "string",
      "id": "string",
      "key": "string",
      "label": "string",
      "links": [
        {}
      ],
      "taskId": "string",
      "workflowRunId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `fieldType` | string |  |
| `id` | string |  |
| `key` | string |  |
| `label` | string |  |
| `links` | array<object> |  |
| `taskId` | string |  |
| `workflowRunId` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `GET /workflow-runs/:workflowRunId/tasks/:taskId/form-fields` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-form-field-values.md) for the provider-specific parameters and requirements.

