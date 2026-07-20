# Readwise: Create Reader Highlight

Creates a new highlight in Readwise Reader.

```
POST https://connect.mindcloud.co/v1/universal/readwise/latest/actions/create-reader-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/create-reader-highlight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.arguments.document_id": "string",
  "params.arguments.html_content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/create-reader-highlight', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.arguments.document_id": "string",
    "params.arguments.html_content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.arguments.document_id` | string | yes | Reader document ID to highlight. |
| `params.arguments.html_content` | string | yes | Exact HTML fragment to highlight. |
| `params.arguments.tags` | string | no | Optional tag names to apply. |
| `params.arguments.note` | string | no | Optional note to attach. |

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

Through the native Readwise API, this operation is `POST https://mcp2.readwise.io/mcp` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reader-highlight.md) for the provider-specific parameters and requirements.

