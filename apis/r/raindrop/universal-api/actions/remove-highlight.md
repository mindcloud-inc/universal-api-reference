# Raindrop: Remove Highlight



```
PUT https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/remove-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/remove-highlight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/remove-highlight', {
  method: 'PUT',
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
| `highlights` | string | no | Array of highlight objects to remove. |
| `id` | string | no | Existing raindrop ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "_id": 1,
        "highlights": [
          {
            "_id": "string",
            "color": "string",
            "created": "string",
            "lastUpdate": "string",
            "note": "string",
            "text": "string"
          }
        ]
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
| `item` | object |  |
| `item._id` | number |  |
| `item.highlights` | array<object> |  |
| `item.highlights[]._id` | string |  |
| `item.highlights[].color` | string |  |
| `item.highlights[].created` | string |  |
| `item.highlights[].lastUpdate` | string |  |
| `item.highlights[].note` | string |  |
| `item.highlights[].text` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `PUT /raindrop/:id` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-highlight.md) for the provider-specific parameters and requirements.

