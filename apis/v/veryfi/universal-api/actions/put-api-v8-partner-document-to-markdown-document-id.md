# Veryfi: Update a Markdown Document

Updates an existing markdown document in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-document-to-markdown-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-document-to-markdown-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-document-to-markdown-document-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `status` | string | no | Update the document status |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "document_type": "string",
      "external_id": "string",
      "id": 1,
      "img_url": "https://example.com",
      "markdown": "string",
      "md_storage_path": "string",
      "pages": [
        {}
      ],
      "pdf_url": "https://example.com",
      "status": "string",
      "tags": [
        "string"
      ],
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `document_type` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `img_url` | string |  |
| `markdown` | string |  |
| `md_storage_path` | string |  |
| `pages` | array<object> |  |
| `pdf_url` | string |  |
| `status` | string |  |
| `tags` | array<string> |  |
| `updated` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/document-to-markdown/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-document-to-markdown-document-id.md) for the provider-specific parameters and requirements.

