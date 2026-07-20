# Veryfi: Create a Tax Line

Creates a tax line in a document in Veryfi.

```
POST https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-documents-document-id-tax-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-documents-document-id-tax-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "boundingRegion[]": [
    1
  ],
  "order": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-documents-document-id-tax-lines', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "boundingRegion[]": [1],
    "order": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `boundingRegion[]` | array<number> | yes | The base amount of the tax applied. number Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `order` | number | yes | The arrangement of tax lines in relation to each other. |

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

Through the native Veryfi API, this operation is `POST /api/v8/partner/documents/:document_id/tax-lines` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-api-v8-partner-documents-document-id-tax-lines.md) for the provider-specific parameters and requirements.

