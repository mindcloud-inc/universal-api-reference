# Weights & Biases: Query Table

Retrieves table rows from Weights & Biases.

```
GET https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/query-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weights & Biases `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/query-table?connectionId=$CONNECTION_ID&digest=string&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "digest": "string",
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/query-table?${params}`, {
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
| `digest` | string | yes | The table digest to query. |
| `project_id` | string | yes | W&B project identifier in entity/project format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rows` | array<object> | Table rows with digest, value, and original index. |

## Native endpoint

Through the native Weights & Biases API, this operation is `POST /table/query` (base URL `https://trace.wandb.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-table.md) for the provider-specific parameters and requirements.

