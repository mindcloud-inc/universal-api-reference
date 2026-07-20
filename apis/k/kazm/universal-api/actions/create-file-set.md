# Kazm: Create File Set

Creates a file set in Kazm.

```
POST https://connect.mindcloud.co/v1/universal/kazm/latest/actions/create-file-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/create-file-set" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kazm/latest/actions/create-file-set', {
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

Through the native Kazm API, this operation is `POST /filesets` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-set.md) for the provider-specific parameters and requirements.

