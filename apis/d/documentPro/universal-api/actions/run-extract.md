# DocumentPro: Run Extract

Starts an extract job in DocumentPro.

```
POST https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/run-extract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocumentPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/run-extract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document_id": "string",
  "template_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/run-extract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document_id": "string",
    "template_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chunk_by_pages` | number | no | Optional page chunk size. |
| `detect_layout` | boolean | no | Whether to detect layout during parsing. |
| `detect_tables` | boolean | no | Whether to detect tables during parsing. |
| `document_id` | string | yes | The document_id to process. |
| `end_regex` | string | no | Optional end regex for splitting. |
| `page_ranges` | string | no | Optional page range selection, for example 1-3. |
| `query_model` | string | no | The query model to use for extraction. |
| `split_regex` | string | no | Optional split regex for parsing segments. |
| `start_regex` | string | no | Optional start regex for splitting. |
| `template_id` | string | yes | The workflow template_id to use for extraction. |
| `use_all_matches` | boolean | no | Whether to use all regex matches. |
| `use_ocr` | boolean | no | Whether to use OCR while parsing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "request_id": "string",
      "request_status": "string",
      "response_body": {},
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |
| `response_body` | object |  |
| `updated_at` | string |  |

## Native endpoint

Through the native DocumentPro API, this operation is `GET /v1/documents/:document_id/run_parser` (base URL `https://api.documentpro.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-extract.md) for the provider-specific parameters and requirements.

