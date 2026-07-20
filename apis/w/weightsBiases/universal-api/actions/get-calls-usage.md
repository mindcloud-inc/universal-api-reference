# Weights & Biases: Get Calls Usage

Retrieves call usage metrics from Weights & Biases.

```
GET https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-calls-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weights & Biases `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-calls-usage?connectionId=$CONNECTION_ID&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-calls-usage?${params}`, {
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
| `project_id` | string | yes | W&B project identifier in entity/project format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call_usage": {},
      "unfinished_call_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call_usage` | object | Aggregated usage metrics keyed by root call ID. |
| `unfinished_call_ids` | array<string> | Root call IDs whose aggregation did not finish. |

## Native endpoint

Through the native Weights & Biases API, this operation is `POST /calls/usage` (base URL `https://trace.wandb.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calls-usage.md) for the provider-specific parameters and requirements.

