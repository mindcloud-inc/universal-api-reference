# Readwise: Set Reader Highlight Notes

Updates notes on a Readwise Reader highlight.

```
PUT https://connect.mindcloud.co/v1/universal/readwise/latest/actions/set-reader-highlight-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/set-reader-highlight-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.arguments.document_id": "string",
  "params.arguments.highlight_document_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/set-reader-highlight-notes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.arguments.document_id": "string",
    "params.arguments.highlight_document_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.arguments.document_id` | string | yes | Reader document ID containing the highlight. |
| `params.arguments.highlight_document_id` | string | yes | Reader highlight document ID. |
| `params.arguments.notes` | string | no | Notes to set for the highlight. Empty clears notes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {}
      ],
      "isError": true,
      "jsonrpc": "string",
      "result": {},
      "structuredContent": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array<object> |  |
| `isError` | boolean |  |
| `jsonrpc` | string |  |
| `result` | object |  |
| `structuredContent` | object |  |

## Native endpoint

Through the native Readwise API, this operation is `POST https://mcp2.readwise.io/mcp` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-reader-highlight-notes.md) for the provider-specific parameters and requirements.

