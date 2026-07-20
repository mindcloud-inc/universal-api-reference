# RightSignature: Send Document From Reusable Template

Sends a document from a RightSignature reusable template.

```
POST https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/send-document-from-reusable-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/send-document-from-reusable-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "roles": {},
  "roles.name": "Ava Chen",
  "mergeFieldValues.value": "string",
  "expiresIn": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/send-document-from-reusable-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "roles": {},
    "roles.name": "Ava Chen",
    "mergeFieldValues.value": "string",
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
| `name` | string | yes | A name for the document you are sending |
| `sharedWith` | list<string> | no | List of email recipients to share the document with |
| `message` | string | no | A message for all signers |
| `inPerson` | boolean | no | Whether the document should be signed in person |
| `callbackUrl` | string | no | Document callback url. The URL will receive a POST for each of the following document events: created , viewed , signed , executed , voided , declined . Note that due to the asynchronous nature of processing, the order in which the document callbacks are sent is not guaranteed. Only HTTP ports 80, 8000-8099, 3000-3009 and HTTPS port 443 is supported. Basic auth is also supported. Ex. “ me:pass@yourhost.example:8001/callback ”. ex. callback when document is viewed { "callbackType":"Document", "id":"edc7823a-7b99-45d7-9c3c-c7dc81f8dbf2", "event":"viewed", "documentState":"pending", "createdAt":"2016-11-14T13:45:23.199-08:00" } |
| `roles` | list<object> | yes | Document signers |
| `roles.name` | string | yes | Role name. For text tags, the role name in the request must correspond to the recipient name given as the second argument (name) in the text tag. When signer sequencing is enabled, the role name must match the signer name set on the template. |
| `roles.signerName` | string | no | Signer name |
| `roles.signerEmail` | string | no | Signer email |
| `roles.signerOmitted` | boolean | no | A signer can be omitted if set to true and if signer_sequencing is enabled |
| `roles.isSender` | boolean | no | Is signer the owner of document? |
| `roles.message` | string | no | Custom message to signer. |
| `mergeFieldIdentifier` | string | no | Merge Field Identifier. By specifying it to “name” API user can map merge field value with the name instead of merge field id |
| `mergeFieldValues` | list<object> | no | Merge Fields |
| `mergeFieldValues.id` | string | no | Merge Field ID |
| `mergeFieldValues.name` | string | no | Merge Field Name. This is the name provided to the merge field on the webapp, while creating the template. If it matches more than one merge field component in template all of them will be filled with the same value |
| `mergeFieldValues.value` | string | yes | Merge Field value. If the merge field is a date, the value should be in yyyy/mm/dd or yyyy-mm-dd format. |
| `expiresIn` | string | yes | Document expiration. Must be between 1 and 365 days |
| `pin` | string | no | Document pin. Must be between 10000 and 99999 |
| `tags` | string | no | Optional key value tags for categorization |
| `kba` | boolean | no | Enable KBA on the document (applicable for KBA enabled plans) |
| `id` | string | yes | Merge Field ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audits": [
        "string"
      ],
      "currentSignerId": "string",
      "embedCodes": "string",
      "executedAt": "string",
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "id": "string",
      "identityMethod": "string",
      "inPerson": true,
      "mergeFieldValues": [
        "string"
      ],
      "name": "Ava Chen",
      "originalFileUrl": "https://example.com",
      "pageImageUrls": [
        "https://example.com"
      ],
      "passcodePinEnabled": true,
      "recipients": [
        {}
      ],
      "sender": {},
      "sentAt": "2026-05-07T12:00:00.000Z",
      "sharedWith": [
        "string"
      ],
      "signedPdfUrl": "https://example.com",
      "state": "string",
      "tags": {},
      "thumbnailUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audits` | array<string> |  |
| `currentSignerId` | string |  |
| `embedCodes` | string |  |
| `executedAt` | string |  |
| `expiredAt` | date |  |
| `filename` | string |  |
| `id` | string |  |
| `identityMethod` | string |  |
| `inPerson` | boolean |  |
| `mergeFieldValues` | array<string> |  |
| `name` | string |  |
| `originalFileUrl` | string |  |
| `pageImageUrls` | array<string> |  |
| `passcodePinEnabled` | boolean |  |
| `recipients` | array<object> |  |
| `sender` | object |  |
| `sentAt` | date |  |
| `sharedWith` | array<string> |  |
| `signedPdfUrl` | string |  |
| `state` | string |  |
| `tags` | object |  |
| `thumbnailUrl` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `POST /reusable_templates/:id/send_document` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-document-from-reusable-template.md) for the provider-specific parameters and requirements.

