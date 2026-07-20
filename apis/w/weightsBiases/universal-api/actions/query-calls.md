# Weights & Biases: Query Calls

Retrieves call records from Weights & Biases.

```
GET https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/query-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weights & Biases `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/query-calls?connectionId=$CONNECTION_ID&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/query-calls?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weights & Biases API returns.

## Native endpoint

Through the native Weights & Biases API, this operation is `POST /calls/stream_query` (base URL `https://trace.wandb.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-calls.md) for the provider-specific parameters and requirements.

