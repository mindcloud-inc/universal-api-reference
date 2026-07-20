# Raindrop: Create Collection



```
POST https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/create-collection', {
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
| `title` | string | no | Name of the collection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "_id": 1,
        "author": true,
        "count": 1,
        "cover": [
          "string"
        ],
        "created": "string",
        "description": "string",
        "expanded": true,
        "lastUpdate": "string",
        "public": true,
        "slug": "string",
        "sort": 1,
        "title": "string",
        "view": "string"
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
| `item.author` | boolean |  |
| `item.count` | number |  |
| `item.cover` | array<string> |  |
| `item.created` | string |  |
| `item.description` | string |  |
| `item.expanded` | boolean |  |
| `item.lastUpdate` | string |  |
| `item.public` | boolean |  |
| `item.slug` | string |  |
| `item.sort` | number |  |
| `item.title` | string |  |
| `item.view` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `POST /collection` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

