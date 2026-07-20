# Microsoft 365 Planner: Get Task Details



```
GET https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-task-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-task-details?connectionId=$CONNECTION_ID&taskId=01gzSlKkIUSUl6DF_EilrmQAKDhh" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "01gzSlKkIUSUl6DF_EilrmQAKDhh"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-task-details?${params}`, {
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
| `taskId` | string | yes | Planner task ID whose details should be retrieved. Example: `01gzSlKkIUSUl6DF_EilrmQAKDhh`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checklist": {},
      "description": "string",
      "id": "string",
      "previewType": "string",
      "references": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checklist` | object |  |
| `description` | string |  |
| `id` | string |  |
| `previewType` | string |  |
| `references` | object |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `GET /v1.0/planner/tasks/{{taskId}}/details` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-details.md) for the provider-specific parameters and requirements.

