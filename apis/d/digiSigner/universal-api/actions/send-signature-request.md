# DigiSigner: Send Signature Request

Creates a signature request in DigiSigner.

```
POST https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/send-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiSigner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/send-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/send-signature-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documents[]` | array<object> | yes | Array of documents to be signed. Each document includes document_id or template id and its signers. |
| `sendEmails` | boolean | no | Whether DigiSigner sends invitation and notification emails. Defaults to true. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `embedded` | boolean | no | Whether documents are embedded on your website. Defaults to false. |
| `redirectForSigningToUrl` | string | no | URL at your website where signers are redirected for signing. |
| `redirectAfterSigningToUrl` | string | no | URL at your website where signers are redirected after signing. |
| `useTextTags` | boolean | no | Whether text tags in documents are converted to fields. Defaults to false. |
| `hideTextTags` | boolean | no | Whether text tags in documents are hidden. Defaults to false. |
| `sendDocumentsAsBundle` | boolean | no | Whether multiple documents should be sent as one bundle. Defaults to false. |
| `bundleTitle` | string | no | Title under which the bundle will be sent to signers. |
| `bundleSubject` | string | no | Subject of the invitation email for the bundled signature request. |
| `bundleMessage` | string | no | Message of the invitation email for the bundled signature request. |

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

Through the native DigiSigner API, this operation is `POST /signature_requests` (base URL `https://api.digisigner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-signature-request.md) for the provider-specific parameters and requirements.

