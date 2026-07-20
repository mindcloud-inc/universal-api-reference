# Xodo Sign: Create Document

Creates a new document in Xodo Sign.

```
POST https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_id": "string",
  "title": "string",
  "files[]": [
    {}
  ],
  "files[].name": "Ava Chen",
  "signers[]": [
    {}
  ],
  "signers[].id": 1,
  "signers[].name": "Ava Chen",
  "signers[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_id": "string",
    "title": "string",
    "files[]": [{}],
    "files[].name": "Ava Chen",
    "signers[]": [{}],
    "signers[].id": 1,
    "signers[].name": "Ava Chen",
    "signers[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `business_id` | string | yes | The Xodo Sign business ID that owns the new document. |
| `sandbox` | boolean | no | Set to 1 to enable sandbox mode for document creation. |
| `is_draft` | boolean | no | Set to 1 to save the document as a draft. |
| `title` | string | yes | Title for the document. |
| `message` | string | no | General document message shown to recipients. |
| `embedded` | boolean | no | Enable embedded requesting for this document. |
| `use_signer_order` | boolean | no | Require signers to sign in the configured order. |
| `reminders` | boolean | no | Enable automatic reminders for the document. |
| `require_all_signers` | boolean | no | Require all signers to complete the document. |
| `files[]` | array<object> | yes | Array of file objects to include in the document. |
| `files[].name` | string | yes | Display name for the uploaded file entry. |
| `files[].file_url` | string | no | Public URL of the file to upload for this file entry. |
| `files[].file_id` | string | no | Previously uploaded Xodo Sign file ID for this file entry. |
| `files[].file_base64` | string | no | Base64-encoded file content for this file entry. |
| `signers[]` | array<object> | yes | Array of signer objects for the document. |
| `signers[].id` | number | yes | Unique signer ID for the signer entry. |
| `signers[].name` | string | yes | Full name of the signer. |
| `signers[].email` | string | yes | Email address of the signer. |
| `signers[].order` | number | no | Signing order number when signer order is enabled. |
| `signers[].pin` | string | no | Optional signer PIN. |
| `signers[].signer_authentication_sms_enabled` | boolean | no | Enable signer SMS authentication for this signer. |
| `signers[].signer_authentication_phone_number` | string | no | Phone number used for signer SMS authentication. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "document_hash": "string",
      "expires": 1,
      "files": [
        {}
      ],
      "is_cancelled": 1,
      "is_completed": 1,
      "is_draft": 1,
      "is_template": 1,
      "log": [
        {}
      ],
      "message": "string",
      "meta": [
        {}
      ],
      "recipients": [
        {}
      ],
      "requester_email": "ava@example.com",
      "signers": [
        {}
      ],
      "subject": "string",
      "template_id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Unix timestamp when the document was created. |
| `document_hash` | string | Unique hash identifier of the created document. |
| `expires` | number | Unix timestamp when the document expires. |
| `files` | array<object> | Files attached to the document. |
| `is_cancelled` | number | 1 when the document is cancelled. |
| `is_completed` | number | 1 when the document is completed. |
| `is_draft` | number | 1 when the document is a draft. |
| `is_template` | number | 1 when the record is a template. |
| `log` | array<object> | Document history entries. |
| `message` | string | Message sent with the document. |
| `meta` | array<object> | Additional metadata entries returned by Xodo Sign. |
| `recipients` | array<object> | Recipients associated with the document. |
| `requester_email` | string | Email address of the document requester. |
| `signers` | array<object> | Signers associated with the document. |
| `subject` | string | Subject of the document. |
| `template_id` | string | Template hash associated with the document when applicable. |
| `title` | string | Title of the document. |

## Native endpoint

Through the native Xodo Sign API, this operation is `POST /document` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

