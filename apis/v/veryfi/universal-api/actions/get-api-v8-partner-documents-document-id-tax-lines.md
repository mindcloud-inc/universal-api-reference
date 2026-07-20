# Veryfi: Returns a list of document Tax Lines

Retrieves tax lines from a document in Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-tax-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-tax-lines?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-tax-lines?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "base": "string",
      "code": "string",
      "name": "Ava Chen",
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
| `code` | string |  |
| `name` | string |  |
| `order` | number |  |
| `rate` | string |  |
| `total` | string |  |
| `total_inclusive` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/documents/:document_id/tax-lines` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-documents-document-id-tax-lines.md) for the provider-specific parameters and requirements.

