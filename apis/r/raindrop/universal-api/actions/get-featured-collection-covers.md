# Raindrop: Get Featured Collection Covers



```
GET https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-featured-collection-covers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-featured-collection-covers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-featured-collection-covers?${params}`, {
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
      "items": [
        {
          "icons": [
            {
              "png": "string",
              "svg": "string"
            }
          ],
          "link": "https://example.com",
          "sort": 1,
          "title": "string"
        }
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].icons` | array<object> |  |
| `items[].icons[].png` | string |  |
| `items[].icons[].svg` | string |  |
| `items[].link` | string |  |
| `items[].sort` | number |  |
| `items[].title` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `GET /collections/covers` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-featured-collection-covers.md) for the provider-specific parameters and requirements.

