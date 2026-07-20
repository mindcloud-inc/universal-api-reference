# Shopkit: List Media

Retrieves media from Shopkit.

```
GET https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-media?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-media?${params}`, {
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
      "checksum": "string",
      "created_at": "string",
      "file_ext": "string",
      "file_name": "Ava Chen",
      "file_size": 1,
      "file_type": "string",
      "id": 1,
      "image_height": 1,
      "image_width": 1,
      "url": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checksum` | string |  |
| `created_at` | string |  |
| `file_ext` | string |  |
| `file_name` | string |  |
| `file_size` | number |  |
| `file_type` | string |  |
| `id` | number |  |
| `image_height` | number |  |
| `image_width` | number |  |
| `url` | object |  |

## Native endpoint

Through the native Shopkit API, this operation is `GET /media` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

