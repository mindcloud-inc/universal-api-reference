# Process Street: Get Workflow Run



```
GET https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/get-workflow-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/get-workflow-run?connectionId=$CONNECTION_ID&workflowRunId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowRunId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/get-workflow-run?${params}`, {
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
      "audit": {},
      "id": "string",
      "links": [
        {}
      ],
      "migrationStatus": "string",
      "name": "Ava Chen",
      "shared": true,
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
| `audit` | object |  |
| `id` | string |  |
| `links` | array<object> |  |
| `migrationStatus` | string |  |
| `name` | string |  |
| `shared` | boolean |  |
| `status` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `GET /workflow-runs/:workflowRunId` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-run.md) for the provider-specific parameters and requirements.

