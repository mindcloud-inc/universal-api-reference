# OneDeck: Create Record

Creates a new record in a OneDeck board.

```
POST https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
  "name": "MindCloud Test Record"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
    "name": "MindCloud Test Record"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | yes | The OneDeck board ID. Example: `1ff5d564-2ea6-4053-8c20-fac2ef32f059`. |
| `name` | string | yes | The name for the new record. Example: `MindCloud Test Record`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldsJson` | string | no | Optional JSON array of field objects to include in the create payload. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneDeck API returns.

## Native endpoint

Through the native OneDeck API, this operation is `POST /boards/{{boardId}}/records` (base URL `https://{{credentials.accountName}}.onedeck.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

