# Priority Matrix: List Item Comments

Retrieves comments for a Priority Matrix item.

```
GET https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-item-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-item-comments?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-item-comments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Priority Matrix item ID. |

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

Through the native Priority Matrix API, this operation is `GET /api/v1/item/:id/comments` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-item-comments.md) for the provider-specific parameters and requirements.

