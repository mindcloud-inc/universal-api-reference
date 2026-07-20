# Kazm: Get File Set

Retrieves a file set from Kazm.

```
GET https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-file-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-file-set?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-file-set?${params}`, {
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
      "file_count": 1,
      "id": "string",
      "indexed_file_count": 1,
      "is_public": true,
      "name": "Ava Chen",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_count` | number |  |
| `id` | string |  |
| `indexed_file_count` | number |  |
| `is_public` | boolean |  |
| `name` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Kazm API, this operation is `GET /filesets/:fileSetId` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-set.md) for the provider-specific parameters and requirements.

