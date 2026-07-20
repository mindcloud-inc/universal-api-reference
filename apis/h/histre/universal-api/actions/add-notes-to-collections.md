# Histre: Add Notes to Collections

Adds notes to collections in Histre.

```
PUT https://connect.mindcloud.co/v1/universal/histre/latest/actions/add-notes-to-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/histre/latest/actions/add-notes-to-collections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urlItemItemIds[]": [
    "https://example.com"
  ],
  "bookIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/histre/latest/actions/add-notes-to-collections', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urlItemItemIds[]": ["https://example.com"],
    "bookIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urlItemItemIds[]` | array<string> | yes | One or more Histre URL item IDs to add to collections. |
| `bookIds[]` | array<string> | yes | One or more Histre collection IDs that should receive the notes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `POST /api/v1/collections/add_notes/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-notes-to-collections.md) for the provider-specific parameters and requirements.

