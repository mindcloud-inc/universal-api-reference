# Monday: Search In Board With Item Name

Finds a board item in Monday by name.

```
POST https://connect.mindcloud.co/v1/universal/monday/latest/actions/search-in-board-with-item-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monday/latest/actions/search-in-board-with-item-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "string",
  "itemName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monday/latest/actions/search-in-board-with-item-name', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "string",
    "itemName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | yes |  |
| `itemName` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Monday API returns.

## Native endpoint

Through the native Monday API, this operation is `POST` (base URL `https://api.monday.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-in-board-with-item-name.md) for the provider-specific parameters and requirements.

