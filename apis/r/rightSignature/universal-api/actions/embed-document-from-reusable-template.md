# RightSignature: Embed Document From Reusable Template

Creates an embeddable document from a RightSignature reusable template.

```
POST https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/embed-document-from-reusable-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/embed-document-from-reusable-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "roles": {},
  "roles.name": "Ava Chen",
  "roles.signerName": "Ava Chen",
  "apiEmbedWidth": "string",
  "apiEmbedHeight": "string",
  "mergeFieldValues.value": "string",
  "expiresIn": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/embed-document-from-reusable-template', {
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
    "roles.signerName": "Ava Chen",
    "apiEmbedWidth": "string",
    "apiEmbedHeight": "string",
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
| `roles` | list<object> | yes | Document signers |
| `roles.name` | string | yes | Role name. For text tags, role name must match. |
| `roles.signerName` | string | yes | Signer name |
| `roles.signerEmail` | string | no | Signer email. |
| `roles.isSender` | boolean | no | Is signer the owner of document? |
| `roles.message` | string | no | Custom message to signer. |
| `apiEmbedWidth` | string | yes | Embed width |
| `apiEmbedHeight` | string | yes | Embed height |
| `mergeFieldIdentifier` | string | no | Merge Field Identifier. By specifying it to “name” API user can map merge field value with the name instead of merge field id |
| `mergeFieldValues` | list<object> | no | Merge Fields |
| `mergeFieldValues.id` | string | no | Merge Field ID |
| `mergeFieldValues.name` | string | no | Merge Field Name. This is the name provided to the merge field on the webapp, while creating the template. If it matches more than one merge field component in template all of them will be filled with the same value |
| `mergeFieldValues.value` | string | yes | Merge Field value. If the merge field is a date, the value should be in yyyy/mm/dd or yyyy-mm-dd format. |
| `expiresIn` | string | yes | Document expiration. Must be between 1 and 365 days |
| `tags` | string | no | Optional key value tags for categorization |
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
      "embedCodes": [
        {}
      ],
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
| `embedCodes` | array<object> |  |
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

Through the native RightSignature API, this operation is `POST /reusable_templates/:id/embed_document` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/embed-document-from-reusable-template.md) for the provider-specific parameters and requirements.

