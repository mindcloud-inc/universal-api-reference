# Raindrop: Create Raindrop



```
POST https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/create-raindrop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/create-raindrop" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/create-raindrop', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collection.$id` | string | no | Destination collection ID. |
| `link` | string | no | Bookmark URL. |
| `title` | string | no | Bookmark title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "_id": 1,
        "collection": {
          "$id": 1
        },
        "cover": "string",
        "created": "string",
        "domain": "string",
        "excerpt": "string",
        "highlights": [
          {}
        ],
        "lastUpdate": "string",
        "link": "https://example.com",
        "note": "string",
        "tags": [
          "string"
        ],
        "title": "string",
        "type": "string"
      },
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item._id` | number |  |
| `item.collection.$id` | number |  |
| `item.cover` | string |  |
| `item.created` | string |  |
| `item.domain` | string |  |
| `item.excerpt` | string |  |
| `item.highlights` | array<object> |  |
| `item.lastUpdate` | string |  |
| `item.link` | string |  |
| `item.note` | string |  |
| `item.tags` | array<string> |  |
| `item.title` | string |  |
| `item.type` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `POST /raindrop` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-raindrop.md) for the provider-specific parameters and requirements.

