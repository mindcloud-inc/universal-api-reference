# Veryfi: Update a Line Item

Updates a line item in a document in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-documents-document-id-line-items-line-item-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-documents-document-id-line-items-line-item-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-documents-document-id-line-items-line-item-id', {
  method: 'PUT',
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
      "description": "string",
      "id": 1,
      "order": 1,
      "price": 1,
      "quantity": 1,
      "tags": [
        "string"
      ],
      "tax": 1,
      "text": "string",
      "total": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `order` | number |  |
| `price` | number |  |
| `quantity` | number |  |
| `tags` | array<string> |  |
| `tax` | number |  |
| `text` | string |  |
| `total` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/documents/:document_id/line-items/:line_item_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-documents-document-id-line-items-line-item-id.md) for the provider-specific parameters and requirements.

