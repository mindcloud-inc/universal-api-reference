# Kazm: Add File To Set

Adds a file to a Kazm file set.

```
POST https://connect.mindcloud.co/v1/universal/kazm/latest/actions/add-file-to-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/add-file-to-set" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kazm/latest/actions/add-file-to-set', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "original_file_name": "Ava Chen",
      "retry_count": 1,
      "size_bytes": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `original_file_name` | string |  |
| `retry_count` | number |  |
| `size_bytes` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Kazm API, this operation is `POST /filesets/:fileSetId/files` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-file-to-set.md) for the provider-specific parameters and requirements.

