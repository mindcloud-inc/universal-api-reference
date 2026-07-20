# DocumentPro: Upload Document

Uploads a document to DocumentPro.

```
POST https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/upload-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocumentPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/upload-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/upload-document', {
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
| `file` | file | yes | The document file to upload. |

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

Through the native DocumentPro API, this operation is `POST /v1/documents` (base URL `https://api.documentpro.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document.md) for the provider-specific parameters and requirements.

