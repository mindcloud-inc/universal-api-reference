# Rendi: List Stored Files

Retrieves stored account files from Rendi.

```
GET https://connect.mindcloud.co/v1/universal/rendi/latest/actions/list-stored-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rendi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/list-stored-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rendi/latest/actions/list-stored-files?${params}`, {
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
      "file_id": "string",
      "is_deleted": true,
      "rendi_store_type": "string",
      "size_mbytes": 1,
      "status": "string",
      "storage_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_id` | string | Unique identifier for a stored file. |
| `is_deleted` | boolean | Whether the file has been deleted. |
| `rendi_store_type` | string | Store type classification (e.g., OUTPUT). |
| `size_mbytes` | number | Stored file size in MB. |
| `status` | string | Storage status of the file. |
| `storage_url` | string | Direct URL to the stored file. |

## Native endpoint

Through the native Rendi API, this operation is `GET /v1/files` (base URL `https://api.rendi.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stored-files.md) for the provider-specific parameters and requirements.

