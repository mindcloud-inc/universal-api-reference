# Emporix Commerce Engine: List Brands

Retrieves brands from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-brands?${params}`, {
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
      "cloudinaryUrl": "https://example.com",
      "description": "string",
      "id": "string",
      "image": "string",
      "localizedDescription": {},
      "localizedName": {},
      "mediaId": "string",
      "metadata": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cloudinaryUrl` | string |  |
| `description` | string |  |
| `id` | string |  |
| `image` | string |  |
| `localizedDescription` | object |  |
| `localizedName` | object |  |
| `mediaId` | string |  |
| `metadata` | object |  |
| `name` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /brand/brands` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-brands.md) for the provider-specific parameters and requirements.

