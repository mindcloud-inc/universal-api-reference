# RightSignature: Prepare Document From Reusable Template

Prepares a document from a RightSignature reusable template.

```
POST https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/prepare-document-from-reusable-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/prepare-document-from-reusable-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roles": {},
  "roles.name": "Ava Chen",
  "expiresIn": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/prepare-document-from-reusable-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roles": {},
    "roles.name": "Ava Chen",
    "expiresIn": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | A name for the document you are sending |
| `sharedWith` | list<string> | no | List of email recipients to share the document with |
| `message` | string | no | A message for all signers |
| `redirectUrl` | string | no | A URL to redirect to after sending the document. Must start with http:// or https://. Example: example.com/redirect |
| `callbackUrl` | string | no | Document callback url. The URL will receive a POST for each of the following document events: created , viewed , signed , executed , voided , declined . Note that due to the asynchronous nature of processing, the order in which the document callbacks are sent is not guaranteed. Only HTTP ports 80, 8000-8099, 3000-3009 and HTTPS port 443 is supported. Basic auth is also supported. Ex. “ me:pass@yourhost.example:8001/callback ”. ex. callback when document is viewed { "callbackType":"Document", "id":"edc7823a-7b99-45d7-9c3c-c7dc81f8dbf2", "event":"viewed", "documentState":"pending", "createdAt":"2016-11-14T13:45:23.199-08:00" } |
| `roles` | list<object> | yes | Document signers |
| `roles.name` | string | yes | Role name. For text tags, the role name in the request must correspond to the recipient name given as the second argument (name) in the text tag. When signer sequencing is enabled, the role name must match the signer name set on the template. |
| `roles.signerName` | string | no | Signer name |
| `roles.signerEmail` | string | no | Signer email |
| `roles.signerOmitted` | boolean | no | A signer can be omitted if set to true and if signer_sequencing is enabled |
| `roles.isSender` | boolean | no | Is signer the owner of document? |
| `roles.message` | string | no | Custom message to signer. |
| `expiresIn` | string | yes | Document expiration. Must be between 1 and 365 days |
| `pin` | string | no | Document pin. Must be between 10000 and 99999 |
| `tags` | string | no | Optional key value tags for categorization |
| `id` | string | yes | Id value |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RightSignature API returns.

## Native endpoint

Through the native RightSignature API, this operation is `POST /reusable_templates/:id/prepare_document` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/prepare-document-from-reusable-template.md) for the provider-specific parameters and requirements.

