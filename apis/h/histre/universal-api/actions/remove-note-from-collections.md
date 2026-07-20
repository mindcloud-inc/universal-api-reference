# Histre: Remove Note from Collections

Removes a note from collections in Histre.

```
PUT https://connect.mindcloud.co/v1/universal/histre/latest/actions/remove-note-from-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/histre/latest/actions/remove-note-from-collections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urlItemItemId": "https://example.com",
  "bookIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/histre/latest/actions/remove-note-from-collections', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urlItemItemId": "https://example.com",
    "bookIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urlItemItemId` | string | yes | Histre URL item ID to remove from the selected collections. |
| `bookIds[]` | array<string> | yes | One or more Histre collection IDs from which the note will be removed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `POST /api/v1/collections/remove_note/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-note-from-collections.md) for the provider-specific parameters and requirements.

