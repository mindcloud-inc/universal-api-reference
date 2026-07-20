# PdfFiller: Create Signature Request From Completed Document

Creates a signature request in PdfFiller from a completed document.

```
POST https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-signature-request-from-completed-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-signature-request-from-completed-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-signature-request-from-completed-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "callbacks": [
        {
          "callback_url": "https://example.com",
          "event_id": "string",
          "id": 1
        }
      ],
      "date_created": 1,
      "date_signed": 1,
      "document_id": 1,
      "document_name": "Ava Chen",
      "envelope_name": "Ava Chen",
      "method": "string",
      "recipients": [
        {
          "access": "string",
          "additional_documents": [
            {
              "files": [
                {
                  "date_created": "string",
                  "filename": "Ava Chen",
                  "id": 1,
                  "ip": "string"
                }
              ],
              "name": "Ava Chen"
            }
          ],
          "date_created": 1,
          "date_signed": 1,
          "email": "ava@example.com",
          "id": 1,
          "ip": "string",
          "message_subject": "string",
          "message_text": "string",
          "name": "Ava Chen",
          "order": 1,
          "phone_authenticate": "string",
          "require_photo": true,
          "roles": [
            {
              "id": 1,
              "name": "Ava Chen"
            }
          ],
          "status": "string",
          "user_id": 1
        }
      ],
      "security_pin": "string",
      "sender_notifications": true,
      "sign_in_order": true,
      "signature_request_id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbacks[].callback_url` | string |  |
| `callbacks[].event_id` | string |  |
| `callbacks[].id` | number |  |
| `date_created` | number |  |
| `date_signed` | number |  |
| `document_id` | number |  |
| `document_name` | string |  |
| `envelope_name` | string |  |
| `method` | string |  |
| `recipients[].access` | string |  |
| `recipients[].additional_documents[].files[].date_created` | string |  |
| `recipients[].additional_documents[].files[].filename` | string |  |
| `recipients[].additional_documents[].files[].id` | number |  |
| `recipients[].additional_documents[].files[].ip` | string |  |
| `recipients[].additional_documents[].name` | string |  |
| `recipients[].date_created` | number |  |
| `recipients[].date_signed` | number |  |
| `recipients[].email` | string |  |
| `recipients[].id` | number |  |
| `recipients[].ip` | string |  |
| `recipients[].message_subject` | string |  |
| `recipients[].message_text` | string |  |
| `recipients[].name` | string |  |
| `recipients[].order` | number |  |
| `recipients[].phone_authenticate` | string |  |
| `recipients[].require_photo` | boolean |  |
| `recipients[].roles[].id` | number |  |
| `recipients[].roles[].name` | string |  |
| `recipients[].status` | string |  |
| `recipients[].user_id` | number |  |
| `security_pin` | string |  |
| `sender_notifications` | boolean |  |
| `sign_in_order` | boolean |  |
| `signature_request_id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native PdfFiller API, this operation is `POST /v2/signature_requests` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signature-request-from-completed-document.md) for the provider-specific parameters and requirements.

