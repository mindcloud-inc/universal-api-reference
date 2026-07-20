# OneDeck: Update Record

Updates an existing record in a OneDeck board.

```
PUT https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
  "recordId": "1ff5d564-2ea6-4053-8c20-fac2ef32f029",
  "updatesJson": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
    "recordId": "1ff5d564-2ea6-4053-8c20-fac2ef32f029",
    "updatesJson": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | yes | The OneDeck board ID. Example: `1ff5d564-2ea6-4053-8c20-fac2ef32f059`. |
| `recordId` | string | yes | The OneDeck record ID. Example: `1ff5d564-2ea6-4053-8c20-fac2ef32f029`. |
| `updatesJson` | string | yes | JSON array of OneDeck update objects with fieldId and value. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneDeck API returns.

## Native endpoint

Through the native OneDeck API, this operation is `PUT /boards/{{boardId}}/records/{{recordId}}` (base URL `https://{{credentials.accountName}}.onedeck.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

