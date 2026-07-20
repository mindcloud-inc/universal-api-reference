# Natif.ai: Upload Document For Capturing

Creates a new document for capturing in Natif.ai.

```
POST https://connect.mindcloud.co/v1/universal/natifai/latest/actions/upload-document-for-capturing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/upload-document-for-capturing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/natifai/latest/actions/upload-document-for-capturing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Document file to upload. Supported file types include jpg, jpeg, tif, tiff, png, pdf, gif, and webp. |
| `language` | string | no | Document language. Defaults to `de`; use `xx` when unknown. Default: `de`. |
| `processDefinitionKey` | string | no | Workflow key to use for processing. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentType` | string | no | Document type. Natif.ai determines the type automatically when omitted. |
| `generatePdf` | list | no | Generate a downloadable PDF from processed pages. One of: `OCR Text Layer`, `ZUGFeRD`. |
| `preview` | boolean | no | Run the upload in preview mode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "doc": "2026-05-07T12:00:00.000Z",
      "document_type": "string",
      "filename_origin": "Ava Chen",
      "language": "string",
      "num_pages": 1,
      "page_num": 1,
      "postprocessing_status": "string",
      "preview": true,
      "process_instance": {},
      "process_instance_id": "string",
      "processing_status": "string",
      "retrieved": true,
      "uploader_username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `doc` | date | Deprecated document timestamp from the API. |
| `document_type` | string |  |
| `filename_origin` | string |  |
| `language` | string |  |
| `num_pages` | number |  |
| `page_num` | number | Deprecated page count field. |
| `postprocessing_status` | string |  |
| `preview` | boolean |  |
| `process_instance` | object |  |
| `process_instance_id` | string |  |
| `processing_status` | string |  |
| `retrieved` | boolean |  |
| `uploader_username` | string | Email of the uploader. |
| `uuid` | string | Unique document ID. |

## Native endpoint

Through the native Natif.ai API, this operation is `POST /documents` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document-for-capturing.md) for the provider-specific parameters and requirements.

