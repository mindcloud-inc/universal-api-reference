# RightSignature: Create Sending Request

Creates a RightSignature sending request for a one-off document.

```
POST https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/create-sending-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/create-sending-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": {},
  "file.name": "Ava Chen",
  "file.source": "string",
  "document": {},
  "document.name": "Ava Chen",
  "document.signerSequencing": true,
  "document.roles": {},
  "document.roles.name": "Ava Chen",
  "document.roles.signerName": "Ava Chen",
  "document.roles.signerEmail": "ava@example.com",
  "document.expiresIn": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/create-sending-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": {},
    "file.name": "Ava Chen",
    "file.source": "string",
    "document": {},
    "document.name": "Ava Chen",
    "document.signerSequencing": true,
    "document.roles": {},
    "document.roles.name": "Ava Chen",
    "document.roles.signerName": "Ava Chen",
    "document.roles.signerEmail": "ava@example.com",
    "document.expiresIn": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | object | yes | Upload file information |
| `file.name` | string | yes | Filename withe extension |
| `file.source` | string | yes | Source of file. Only 'upload' is supported. |
| `document` | object | yes | Document information |
| `document.name` | string | yes | Document name |
| `document.signerSequencing` | boolean | yes | Send to signers in specified sequence. |
| `document.personalizedMessages` | boolean | no | Use custom messages per signer. Specified in 'roles' attribute. |
| `document.sharedWith` | list<string> | no | Array of emails to CC document. |
| `document.identityMethod` | string | no | How to authenticate signers (email \| none). |
| `document.callbackUrl` | string | no | Document callback url. The URL will receive a POST for each of the following document events: created , viewed , signed , executed , voided , declined . Note that due to the asynchronous nature of processing, the order in which the document callbacks are sent is not guaranteed. Only HTTP ports 80, 8000-8099, 3000-3009 and HTTPS port 443 is supported. Basic auth is also supported. Ex. “ me:pass@yourhost.example:8001/callback ”. Note : This is different from the sending request callback url which receives status updates regarding the sending request itself. ex. callback when document is viewed { "callbackType": "Document" , "id": "edc7823a-7b99-45d7-9c3c-c7dc81f8dbf2" , "event": "viewed" , "documentState": "pending" , "createdAt": "2016-11-14T13:45:23.199-08:00" } |
| `document.apiEmbedded` | boolean | no | Whether the document should be embedded. |
| `document.apiEmbedWidth` | string | no | Embed width |
| `document.apiEmbedHeight` | string | no | Embed height |
| `document.roles` | list<object> | yes | Document signers |
| `document.roles.name` | string | yes | Role name. For text tags, the role name in the request must correspond to the recipient name given as the second argument (name) in the text tag. When signer sequencing is enabled, the role name must match the signer name set on the template. |
| `document.roles.signerName` | string | yes | Signer name |
| `document.roles.isSender` | boolean | no | Is signer the owner of document? |
| `document.roles.sequence` | number | no | Signer order (starting at 0), required if signer_sequencing is enabled. |
| `document.roles.message` | string | no | Custom message to signer. |
| `document.roles.signerEmail` | string | yes | Signer email |
| `document.expiresIn` | string | yes | Document expiration. Must be between 1 and 365 days |
| `document.pin` | string | no | Document pin. Must be between 10000 and 99999 |
| `document.tags` | string | no | Optional key value tags for categorization |
| `document.kba` | boolean | no | Enable KBA on the document (applicable for KBA enabled plans) |
| `callbackUrl` | string | no | URL to receive sending request status updates. The URL will receive a POST when the sending request is sent as a document or an error occured in processing. Only HTTP ports 80, 8000-8099, 3000-3009 and HTTPS port 443 is supported. Basic auth is also supported. Ex. value: “ me:pass@yourhost.example/req_callback ” ex. callback when successful { "sending_request": { "id": "09001350-1853-471c-955a-abb7d3120aa1", "status": "completed", "document_template_id": "733816f6-939f-4a8d-98de-55e357ab07d4", "created_at":"2016-08-10T18:57:29.400-07:00", "updated_at":"2016-08-10T19:05:11.100-07:00" } } ex. callback when processing fails { "sending_request": { "id": "09001350-1853-471c-955a-abb7d3120aa1", "status": "errored", "status_message": "File was password protected" "document_template_id": null, "created_at":"2016-08-10T18:57:29.400-07:00", "updated_at":"2016-08-10T19:05:11.100-07:00" } } |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "documentTemplateId": "string",
      "id": "string",
      "status": "string",
      "statusMessage": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `documentTemplateId` | string |  |
| `id` | string |  |
| `status` | string |  |
| `statusMessage` | string |  |
| `updatedAt` | date |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `POST /sending_requests` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sending-request.md) for the provider-specific parameters and requirements.

