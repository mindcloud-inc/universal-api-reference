# Skribble: Create Signature Request

Creates a signature request in Skribble.

```
POST https://connect.mindcloud.co/v1/universal/skribble/latest/actions/create-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/create-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribble/latest/actions/create-signature-request', {
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
| `attachOnSuccess[]` | array<string> | no | Artifacts to attach automatically after signing succeeds. |
| `callbackErrorUrl` | string | no | Callback URL for callback or signing errors. |
| `callbackSuccessUrl` | string | no | Callback URL for successful completion. |
| `callbackUpdateUrl` | string | no | Callback URL for status updates. |
| `ccEmailAddresses[]` | array<string> | no | Observer email addresses to notify. |
| `content` | string | no | The base64 encoded PDF content. |
| `contentType` | string | no | Optional MIME type for the uploaded content. |
| `creator` | string | no | Specific business member who should own the signature request. |
| `documentId` | string | no | Existing Skribble document ID to sign. |
| `fileUrl` | string | no | Public URL of the PDF to sign instead of uploading content. |
| `legislation` | string | no | Requested legislation such as ZERTES. |
| `message` | string | no | Optional message shown to signers. |
| `quality` | string | no | Requested signature quality such as SES or AES. |
| `signatures[]` | array<object> | no | Signer objects including emails, sequence, and optional visual signature settings. |
| `title` | string | no | The signature request title. |
| `writeAccess[]` | array<string> | no | Users allowed to add signers later when creating without initial signers. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skribble API returns.

## Native endpoint

Through the native Skribble API, this operation is `POST /v2/signature-requests` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signature-request.md) for the provider-specific parameters and requirements.

