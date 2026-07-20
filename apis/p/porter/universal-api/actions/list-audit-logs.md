# Porter: List Audit Logs

Retrieves audit logs from a Porter project.

```
GET https://connect.mindcloud.co/v1/universal/porter/latest/actions/list-audit-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porter/latest/actions/list-audit-logs?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porter/latest/actions/list-audit-logs?${params}`, {
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
| `projectId` | string | yes | The Porter project ID whose audit logs you want to list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Porter API returns.

## Native endpoint

Through the native Porter API, this operation is `GET /api/v2/projects/:projectId/audit-logs` (base URL `https://dashboard.porter.run`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audit-logs.md) for the provider-specific parameters and requirements.

