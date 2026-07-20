# Deep Infra: Query Inference Logs



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/query-inference-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/query-inference-logs?connectionId=$CONNECTION_ID&deployId=DpM4BkrjEspUwmTa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deployId": "DpM4BkrjEspUwmTa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/query-inference-logs?${params}`, {
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
| `deployId` | string | yes | Deployment ID whose inference logs should be queried. Example: `DpM4BkrjEspUwmTa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completion_tokens": 1,
      "cost": 1,
      "created_at": "string",
      "deploy_id": "string",
      "model": "string",
      "prompt_tokens": 1,
      "request_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completion_tokens` | number | Output token count when returned. |
| `cost` | number | Estimated request cost when returned. |
| `created_at` | string | Log creation timestamp. |
| `deploy_id` | string | Deployment identifier for the log row. |
| `model` | string | Model used for the inference request. |
| `prompt_tokens` | number | Input token count when returned. |
| `request_id` | string | Inference request identifier. |
| `status` | string | Inference request status. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/logs/query` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-inference-logs.md) for the provider-specific parameters and requirements.

