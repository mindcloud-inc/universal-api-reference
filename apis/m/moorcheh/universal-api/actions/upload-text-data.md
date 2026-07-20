# Moorcheh: Upload Text Data

Uploads text documents to a Moorcheh namespace.

```
POST https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/upload-text-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/upload-text-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespace_name": "Ava Chen",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/upload-text-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "namespace_name": "Ava Chen",
    "documents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespace_name` | string | yes | Name of the text namespace to upload documents to. |
| `documents[]` | array<object> | yes | Array of flat document objects with id, text, and optional metadata fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_ids": [
        "string"
      ],
      "execution_time": 1,
      "message": "string",
      "queued_documents": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_ids` | array<string> | Document IDs accepted by Moorcheh. |
| `execution_time` | number | Request execution time in seconds. |
| `message` | string | Human-readable upload message. |
| `queued_documents` | number | Number of documents queued for processing. |
| `status` | string | Upload queue status. |

## Native endpoint

Through the native Moorcheh API, this operation is `POST /namespaces/:namespace_name/documents` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-text-data.md) for the provider-specific parameters and requirements.

