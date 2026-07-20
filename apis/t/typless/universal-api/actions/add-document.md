# Typless: Add Document



```
POST https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "learning_fields": {},
  "file_name": "Ava Chen",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "learning_fields": {},
    "file_name": "Ava Chen",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `learning_fields` | object | yes | Ground-truth learning fields for the document being added to the dataset. |
| `file_name` | string | yes | Original filename of the document being added to the dataset. |
| `file` | string | yes | Base64-encoded file content for the dataset document. |
| `document_type_name` | string | no | Optional Typless document type name for the dataset document. |
| `line_items` | object | no | Optional line item ground-truth values for the dataset document. |
| `vat_rates` | object | no | Optional VAT rate ground-truth values for the dataset document. |

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
| `details` | array<string> | Document object identifiers returned by Typless. |
| `message` | string | Document add result message. |

## Native endpoint

Through the native Typless API, this operation is `POST /api/v1/add-document` (base URL `https://developers.typless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-document.md) for the provider-specific parameters and requirements.

