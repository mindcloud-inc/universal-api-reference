# v0: Find Deployment Logs

Finds logs for a v0 deployment.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-deployment-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-deployment-logs?connectionId=$CONNECTION_ID&deploymentId=dpl_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentId": "dpl_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-deployment-logs?${params}`, {
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
| `deploymentId` | string | yes | Use the canonical dpl_... deployment ID returned by Find Deployments, not the bare token from the inspector URL. Example: `dpl_abc123`. |
| `since` | number | no | Use the nextSince value returned by this action when paginating. Live verification showed the API expects a 13-digit millisecond timestamp in practice. Example: `1774287206570`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deploymentId": "string",
      "id": "string",
      "level": "string",
      "object": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deploymentId` | string |  |
| `id` | string |  |
| `level` | string |  |
| `object` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/deployments/:deploymentId/logs` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-deployment-logs.md) for the provider-specific parameters and requirements.

