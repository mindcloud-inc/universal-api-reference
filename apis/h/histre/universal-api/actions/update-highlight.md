# Histre: Update a Highlight

Updates a highlight in Histre.

```
PUT https://connect.mindcloud.co/v1/universal/histre/latest/actions/update-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/histre/latest/actions/update-highlight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "highlightId": "string",
  "text": "string",
  "color": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/histre/latest/actions/update-highlight', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "highlightId": "string",
    "text": "string",
    "color": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `highlightId` | string | yes | Identifier of the highlight to update. |
| `text` | string | yes | Updated highlighted text. |
| `color` | string | yes | Updated highlight color. |
| `extra` | object | no | Optional updated extra highlight details. |
| `note` | string | no | Optional updated note text. Pass null or empty string to remove it. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `PATCH /api/v1/highlight/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-highlight.md) for the provider-specific parameters and requirements.

