# Priority Matrix: Add Item Comment

Creates a new comment on a Priority Matrix item.

```
POST https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/add-item-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/add-item-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "item": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/add-item-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "item": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item` | string | yes | Item resource URI, for example /api/v1/item/345/. |
| `text` | string | yes | Comment text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "id": 1,
      "item": "string",
      "resource_uri": "string",
      "text": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `id` | number |  |
| `item` | string |  |
| `resource_uri` | string |  |
| `text` | string |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `POST /api/v1/comment/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-item-comment.md) for the provider-specific parameters and requirements.

