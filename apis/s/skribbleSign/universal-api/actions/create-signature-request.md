# Skribble Sign: Create Signature Request

Creates a new signature request in Skribble Sign.

```
POST https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-signature-request', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | The signature request title. |
| `message` | string | no | Optional message shown to signers. |
| `content` | string | no | The base64 encoded PDF content. |
| `contentType` | string | no | Optional MIME type for the uploaded content. |
| `fileUrl` | string | no | Public URL of the PDF to sign instead of uploading content. |
| `documentId` | string | no | Existing Skribble document ID to sign. |
| `quality` | string | no | Requested signature quality such as SES or AES. |
| `legislation` | string | no | Requested legislation such as ZERTES. |
| `signatures[]` | array<object> | no | Signer objects including emails, sequence, and optional visual signature settings. |
| `writeAccess[]` | array<string> | no | Users allowed to add signers later when creating without initial signers. |
| `ccEmailAddresses[]` | array<string> | no | Observer email addresses to notify. |
| `attachOnSuccess[]` | array<string> | no | Artifacts to attach automatically after signing succeeds. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `creator` | string | no | Specific business member who should own the signature request. |
| `callbackSuccessUrl` | string | no | Callback URL for successful completion. |
| `callbackUpdateUrl` | string | no | Callback URL for status updates. |
| `callbackErrorUrl` | string | no | Callback URL for callback or signing errors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "signatures": [
        {}
      ],
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Signature request ID. |
| `signatures` | array<object> | Signature entries. |
| `status` | string | Signature request status. |
| `title` | string | Signature request title. |

## Native endpoint

Through the native Skribble Sign API, this operation is `POST /v2/signature-requests` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signature-request.md) for the provider-specific parameters and requirements.

