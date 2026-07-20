# Raindrop: Get All Highlights



```
GET https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-all-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-all-highlights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-all-highlights?${params}`, {
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
      "count": 1,
      "items": [
        {
          "_id": "string",
          "color": "string",
          "created": "string",
          "link": "https://example.com",
          "note": "string",
          "raindropRef": 1,
          "tags": [
            "string"
          ],
          "text": "string",
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
| `count` | number |  |
| `items` | array<object> |  |
| `items[]._id` | string |  |
| `items[].color` | string |  |
| `items[].created` | string |  |
| `items[].link` | string |  |
| `items[].note` | string |  |
| `items[].raindropRef` | number |  |
| `items[].tags` | array<string> |  |
| `items[].text` | string |  |
| `items[].title` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `GET /highlights` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-highlights.md) for the provider-specific parameters and requirements.

