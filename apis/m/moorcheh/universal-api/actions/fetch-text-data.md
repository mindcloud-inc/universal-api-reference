# Moorcheh: Fetch Text Data

Retrieves text chunks from a Moorcheh namespace with cursor pagination.

```
GET https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/fetch-text-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/fetch-text-data?connectionId=$CONNECTION_ID&namespace_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/fetch-text-data?${params}`, {
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
| `namespace_name` | string | yes | Name of the text namespace to fetch text chunks from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "execution_time": 1,
      "items": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "is_summary": true,
          "metadata": {},
          "text": "string"
        }
      ],
      "message": "string",
      "namespace": "Ava Chen",
      "statistics": {
        "source_counts": {},
        "total_items": 1,
        "total_summary_chunks": 1,
        "total_text_chunks": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `execution_time` | number | Execution time in seconds. |
| `items` | array<object> | Fetched text chunks. |
| `items[].created_at` | date | Creation timestamp. |
| `items[].id` | string | Chunk or document ID. |
| `items[].is_summary` | boolean | Whether this item is a summary chunk. |
| `items[].metadata` | object | Chunk metadata. |
| `items[].text` | string | Chunk text. |
| `message` | string | Human-readable fetch message. |
| `namespace` | string | Requested namespace. |
| `statistics` | object | Aggregated counts and timestamps. |
| `statistics.source_counts` | object | Counts by source. |
| `statistics.total_items` | number | Returned item count. |
| `statistics.total_summary_chunks` | number | Summary chunk count. |
| `statistics.total_text_chunks` | number | Non-summary chunk count. |
| `status` | string | Fetch status. |

## Native endpoint

Through the native Moorcheh API, this operation is `GET /namespaces/:namespace_name/documents/fetch-text-data` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-text-data.md) for the provider-specific parameters and requirements.

