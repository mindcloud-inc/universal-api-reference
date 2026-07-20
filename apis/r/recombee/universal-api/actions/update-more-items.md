# Recombee: Update More Items

Updates multiple items in your Recombee catalog.

```
PUT https://connect.mindcloud.co/v1/universal/recombee/latest/actions/update-more-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/update-more-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "changes": "[object Object]",
  "filter": "price > 100"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recombee/latest/actions/update-more-items', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "changes": "[object Object]",
    "filter": "price > 100"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `changes` | object | yes | Example: `[object Object]`. |
| `filter` | string | yes | Example: `price > 100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "itemIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of items updated by the request. |
| `itemIds` | array<string> | IDs of the items updated by the request. |

## Native endpoint

Through the native Recombee API, this operation is `POST /more-items/` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-more-items.md) for the provider-specific parameters and requirements.

