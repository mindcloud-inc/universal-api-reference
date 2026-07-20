# xAI: List Batch Results

Retrieves batch results from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/list-batch-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/list-batch-results?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/list-batch-results?${params}`, {
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
| `batch_id` | string | no | Batch identifier whose results should be listed. |
| `pagination_token` | string | no | Page token from a previous list results response. |
| `limit` | number | no | Maximum results to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination_token": "string",
      "results": [
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
| `pagination_token` | string |  |
| `results` | array<object> |  |

## Native endpoint

Through the native xAI API, this operation is `GET /batches/:batch_id/results` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-batch-results.md) for the provider-specific parameters and requirements.

