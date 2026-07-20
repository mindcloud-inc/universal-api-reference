# Deep Infra: Query Deployment Logs



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/query-deployment-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/query-deployment-logs?connectionId=$CONNECTION_ID&deployId=DpM4BkrjEspUwmTa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deployId": "DpM4BkrjEspUwmTa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/query-deployment-logs?${params}`, {
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
| `deployId` | string | yes | Deployment ID whose deployment logs should be queried. Example: `DpM4BkrjEspUwmTa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deploy_id": "string",
      "level": "string",
      "message": "string",
      "request_id": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deploy_id` | string | Deployment identifier. |
| `level` | string | Log level. |
| `message` | string | Log message. |
| `request_id` | string | Related request identifier when returned. |
| `timestamp` | string | Log timestamp. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/deployment_logs/query` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-deployment-logs.md) for the provider-specific parameters and requirements.

