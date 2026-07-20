# Veryfi: Returns document Tax Line

Retrieves a tax line from a document in Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-tax-lines-tax-line-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-tax-lines-tax-line-id?connectionId=$CONNECTION_ID&documentId=string&taxLineId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "taxLineId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-tax-lines-tax-line-id?${params}`, {
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
| `taxLineId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base": "string",
      "code": {},
      "name": {},
      "order": 1,
      "rate": "string",
      "total": "string",
      "total_inclusive": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base` | string |  |
| `code` | object |  |
| `name` | object |  |
| `order` | number |  |
| `rate` | string |  |
| `total` | string |  |
| `total_inclusive` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/documents/:document_id/tax-lines/:tax_line_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-documents-document-id-tax-lines-tax-line-id.md) for the provider-specific parameters and requirements.

