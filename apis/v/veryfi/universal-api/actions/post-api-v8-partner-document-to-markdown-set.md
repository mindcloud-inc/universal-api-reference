# Veryfi: Process a Markdown Document Set

Creates markdown documents by splitting files in Veryfi.

```
POST https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-document-to-markdown-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-document-to-markdown-set" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-document-to-markdown-set', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "document_ids": [
        1
      ],
      "id": 1,
      "page_breaks": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_ids` | array<number> |  |
| `id` | number |  |
| `page_breaks` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `POST /api/v8/partner/document-to-markdown-set` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-api-v8-partner-document-to-markdown-set.md) for the provider-specific parameters and requirements.

