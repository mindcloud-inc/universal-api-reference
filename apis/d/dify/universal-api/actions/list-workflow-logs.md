# Dify: List Workflow Logs

Retrieves workflow logs from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-workflow-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-workflow-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-workflow-logs?${params}`, {
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
| `page` | number | no | Page number to return. |
| `keyword` | string | no | Keyword filter for workflow logs. |
| `status` | string | no | Workflow run status filter. |
| `createdAtBefore` | string | no | Return logs created before this timestamp. |
| `createdAtAfter` | string | no | Return logs created after this timestamp. |
| `createdByEndUserSessionId` | string | no | Filter by end-user session ID. |
| `createdByAccount` | string | no | Filter by creator account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "createdByAccount": "string",
      "createdByEndUser": {},
      "createdByRole": "string",
      "createdFrom": "string",
      "id": "string",
      "workflowRun": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `createdByAccount` | string |  |
| `createdByEndUser` | object |  |
| `createdByRole` | string |  |
| `createdFrom` | string |  |
| `id` | string |  |
| `workflowRun` | object |  |

## Native endpoint

Through the native Dify API, this operation is `GET /workflows/logs` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-logs.md) for the provider-specific parameters and requirements.

