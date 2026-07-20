# DocumentPro: Confirm Uploaded Document

Confirms a large uploaded document in DocumentPro.

```
POST https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/confirm-uploaded-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocumentPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/confirm-uploaded-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_extension": "string",
  "file_name": "Ava Chen",
  "upload_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/confirm-uploaded-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_extension": "string",
    "file_name": "Ava Chen",
    "upload_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_extension` | string | yes | The uploaded file extension, for example pdf. |
| `file_name` | string | yes | The original file name for the uploaded file. |
| `upload_url` | string | yes | The temporary upload URL returned by Get Large Upload URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "document_id": "string",
      "file_extension": "string",
      "file_name": "Ava Chen",
      "meta_tags": {},
      "num_pages": 1,
      "parser_runs": [
        {}
      ],
      "source_name": "Ava Chen",
      "updated_at": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `document_id` | string |  |
| `file_extension` | string |  |
| `file_name` | string |  |
| `meta_tags` | object |  |
| `num_pages` | number |  |
| `parser_runs` | array<object> |  |
| `source_name` | string |  |
| `updated_at` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native DocumentPro API, this operation is `POST /v1/documents` (base URL `https://api.documentpro.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-uploaded-document.md) for the provider-specific parameters and requirements.

