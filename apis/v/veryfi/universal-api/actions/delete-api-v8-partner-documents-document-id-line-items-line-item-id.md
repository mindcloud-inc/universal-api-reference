# Veryfi: Delete a Line Item

Deletes a line item from a document in Veryfi.

```
DELETE https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-documents-document-id-line-items-line-item-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-documents-document-id-line-items-line-item-id?connectionId=$CONNECTION_ID&documentId=string&lineItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "lineItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-documents-document-id-line-items-line-item-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `lineItemId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": [
        {}
      ],
      "error": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | array<object> |  |
| `error` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `DELETE /api/v8/partner/documents/:document_id/line-items/:line_item_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-api-v8-partner-documents-document-id-line-items-line-item-id.md) for the provider-specific parameters and requirements.

