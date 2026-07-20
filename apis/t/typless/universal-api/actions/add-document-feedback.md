# Typless: Add Document Feedback



```
POST https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document_type_name": "Ava Chen",
  "learning_fields": {},
  "document_object_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document_type_name": "Ava Chen",
    "learning_fields": {},
    "document_object_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document_type_name` | string | yes | Typless document type name for the document feedback. |
| `learning_fields` | object | yes | Corrected learning fields for the reviewed document. |
| `document_object_id` | string | yes | Typless dataset document object identifier. |
| `line_items` | object | no | Optional corrected line item values for the reviewed document. |
| `vat_rates` | object | no | Optional corrected VAT rate values for the reviewed document. |

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
| `details` | array<string> | Document object identifiers updated by the feedback call. |
| `message` | string | Feedback result message. |

## Native endpoint

Through the native Typless API, this operation is `POST /api/v1/add-document-feedback` (base URL `https://developers.typless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-document-feedback.md) for the provider-specific parameters and requirements.

