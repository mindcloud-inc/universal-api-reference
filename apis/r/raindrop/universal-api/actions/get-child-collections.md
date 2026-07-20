# Raindrop: Get Child Collections



```
GET https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-child-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-child-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-child-collections?${params}`, {
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
          "_id": 1,
          "count": 1,
          "cover": [
            "string"
          ],
          "created": "string",
          "expanded": true,
          "lastUpdate": "string",
          "public": true,
          "sort": 1,
          "title": "string",
          "view": "string"
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
| `items[]._id` | number |  |
| `items[].count` | number |  |
| `items[].cover` | array<string> |  |
| `items[].created` | string |  |
| `items[].expanded` | boolean |  |
| `items[].lastUpdate` | string |  |
| `items[].public` | boolean |  |
| `items[].sort` | number |  |
| `items[].title` | string |  |
| `items[].view` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `GET /collections/childrens` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-child-collections.md) for the provider-specific parameters and requirements.

