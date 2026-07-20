# Typless: Add Document Async



```
POST https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document-async
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document-async" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_name": "Ava Chen",
  "file": "string",
  "document_type_name": "Ava Chen",
  "learning_fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document-async', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_name": "Ava Chen",
    "file": "string",
    "document_type_name": "Ava Chen",
    "learning_fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_name` | string | yes | Original filename of the dataset document being added asynchronously. |
| `file` | string | yes | Base64-encoded file content for the async dataset document. |
| `document_type_name` | string | yes | Typless document type name for the async dataset document. |
| `learning_fields` | object | yes | Ground-truth learning fields for the async dataset document. |
| `line_items` | object | no | Optional line item ground-truth values for the async dataset document. |
| `vat_rates` | object | no | Optional VAT rate ground-truth values for the async dataset document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": [
        "string"
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | array<string> | Async dataset task identifiers returned by Typless. |
| `message` | string | Async document addition result message. |

## Native endpoint

Through the native Typless API, this operation is `POST /api/v1/add-document-async` (base URL `https://developers.typless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-document-async.md) for the provider-specific parameters and requirements.

