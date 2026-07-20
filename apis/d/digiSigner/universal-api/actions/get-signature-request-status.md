# DigiSigner: Get Signature Request Status

Retrieves a DigiSigner signature request by ID.

```
GET https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-signature-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiSigner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-signature-request-status?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-signature-request-status?${params}`, {
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
| `signatureRequestId` | string | yes | DigiSigner signature_request_id returned by Send Signature Request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "embedded": true,
      "hide_text_tags": true,
      "is_completed": true,
      "send_documents_as_bundle": true,
      "send_emails": true,
      "send_reminder_emails": true,
      "signature_request_id": "string",
      "use_text_tags": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> | Documents included in the signature request. |
| `embedded` | boolean | Whether the request is for embedded signing. |
| `hide_text_tags` | boolean | Whether text tags were hidden. |
| `is_completed` | boolean | Whether all signers completed all documents. |
| `send_documents_as_bundle` | boolean | Whether documents are delivered as a bundle. |
| `send_emails` | boolean | Whether invitation and notification emails are sent. |
| `send_reminder_emails` | boolean | Whether DigiSigner sends reminder emails for the request. |
| `signature_request_id` | string | Signature request identifier. |
| `use_text_tags` | boolean | Whether text tags were converted to fields. |

## Native endpoint

Through the native DigiSigner API, this operation is `GET /signature_requests/:signatureRequestId` (base URL `https://api.digisigner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature-request-status.md) for the provider-specific parameters and requirements.

