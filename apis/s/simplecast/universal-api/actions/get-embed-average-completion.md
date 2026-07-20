# Simplecast: Get Embed Average Completion

Retrieves embed average completion analytics from Simplecast.

```
GET https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-embed-average-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-embed-average-completion?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-embed-average-completion?${params}`, {
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
      "collection": [
        {}
      ],
      "count": 1,
      "data": {},
      "description": "string",
      "href": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "title": "string",
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> |  |
| `count` | number |  |
| `data` | object |  |
| `description` | string |  |
| `href` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `title` | string |  |
| `total` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Simplecast API, this operation is `GET /analytics/embed/avg_completion` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-embed-average-completion.md) for the provider-specific parameters and requirements.

