# Veryfi: Get a Document

Retrieves a document from Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id?${params}`, {
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
| `boundingBoxes` | boolean | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidenceDetails` | boolean | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
| `detailed` | boolean | no | This field was deprecated on 2023-08-20. Use bounding_boxes and confidence_details . |
| `returnAuditTrail` | boolean | no | Deprecated. |

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
      "message": "string",
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
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/documents/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-documents-document-id.md) for the provider-specific parameters and requirements.

