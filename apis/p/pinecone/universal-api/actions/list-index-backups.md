# Pinecone: List Index Backups

Retrieves backups for a Pinecone index.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-index-backups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-index-backups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-index-backups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "backup_id": "string",
          "cloud": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "dimension": 1,
          "name": "Ava Chen",
          "namespace_count": 1,
          "record_count": 1,
          "region": "string",
          "size_bytes": 1,
          "source_index_id": "string",
          "source_index_name": "Ava Chen",
          "status": "string"
        }
      ],
      "pagination": {
        "next": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].backup_id` | string |  |
| `data[].cloud` | string |  |
| `data[].created_at` | date |  |
| `data[].description` | string |  |
| `data[].dimension` | number |  |
| `data[].name` | string |  |
| `data[].namespace_count` | number |  |
| `data[].record_count` | number |  |
| `data[].region` | string |  |
| `data[].size_bytes` | number |  |
| `data[].source_index_id` | string |  |
| `data[].source_index_name` | string |  |
| `data[].status` | string |  |
| `pagination.next` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /indexes/:index_name/backups` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-index-backups.md) for the provider-specific parameters and requirements.

