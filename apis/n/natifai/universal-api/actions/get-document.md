# Natif.ai: Get Document

Retrieves a document and its processing status from Natif.ai.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | UUID of the document. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `getProcessInstance` | boolean | no | Return detailed processing information for workflow-processed documents. |

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

Through the native Natif.ai API, this operation is `GET /documents/[:documentId]` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

