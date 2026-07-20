# Goody: List Cards

Retrieves active cards from Goody.

```
GET https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goody `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-cards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-cards?${params}`, {
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
      "id": "string",
      "image": {
        "height": 1,
        "url": "https://example.com",
        "width": 1
      },
      "image_thumb": {
        "height": 1,
        "url": "https://example.com",
        "width": 1
      },
      "occasions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `image` | object |  |
| `image_thumb` | object |  |
| `image_thumb.height` | number |  |
| `image_thumb.url` | string |  |
| `image_thumb.width` | number |  |
| `image.height` | number |  |
| `image.url` | string |  |
| `image.width` | number |  |
| `occasions` | array<string> |  |

## Native endpoint

Through the native Goody API, this operation is `GET /v1/cards` (base URL `https://api.ongoody.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cards.md) for the provider-specific parameters and requirements.

