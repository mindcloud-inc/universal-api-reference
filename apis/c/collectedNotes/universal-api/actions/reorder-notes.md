# Collected Notes: Reorder Notes



```
PUT https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/reorder-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/reorder-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": 1,
  "ids": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/reorder-notes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": 1,
    "ids": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | number | yes | The Collected Notes site ID. |
| `ids` | string | yes | Send the sorted note IDs as a JSON-like array string, for example [1,2,3]. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Collected Notes API returns.

## Native endpoint

Through the native Collected Notes API, this operation is `GET /sites/:siteId/notes/reorder` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reorder-notes.md) for the provider-specific parameters and requirements.

