# Deep Infra: List OpenAI Batches



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-batches?connectionId=$CONNECTION_ID&after=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "after": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-batches?${params}`, {
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
| `after` | string | yes | Batch pagination cursor from the DeepInfra OpenAI batches API. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of batches to return. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completion_window": "string",
      "created_at": 1,
      "endpoint": "string",
      "error_file_id": "string",
      "errors": {},
      "id": "string",
      "input_file_id": "string",
      "object": "string",
      "output_file_id": "string",
      "request_counts": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completion_window` | string | Requested completion window. |
| `created_at` | number | Batch creation timestamp. |
| `endpoint` | string | Batch endpoint. |
| `error_file_id` | string | Error file identifier when present. |
| `errors` | object | Batch error details when present. |
| `id` | string | Batch identifier. |
| `input_file_id` | string | Input file identifier. |
| `object` | string | OpenAI-compatible batch object type. |
| `output_file_id` | string | Output file identifier when complete. |
| `request_counts` | object | Batch request count summary. |
| `status` | string | Batch status. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/batches` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-open-ai-batches.md) for the provider-specific parameters and requirements.

