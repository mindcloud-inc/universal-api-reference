# SignRequest: Quick Create SignRequest



```
POST https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/quick-create-sign-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/quick-create-sign-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signers[]": [
    {}
  ],
  "signers[].email": "signer@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/quick-create-sign-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signers[]": [{}],
    "signers[].email": "signer@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileFromUrl` | string | no | Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `name` | string | no | Example: `customer-agreement.pdf`. |
| `signers[]` | array<object> | yes |  |
| `signers[].email` | string | yes | Example: `signer@example.com`. |
| `fromEmail` | string | no | Example: `legal@example.com`. |
| `subject` | string | no | Example: `Please sign this agreement`. |
| `message` | string | no | Example: `Please review and sign when ready.`. |
| `disableEmails` | boolean | no |  |
| `who` | list<string> | no | One of: `m`, `mo`, `o`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileFromContent` | string | no | Example: `JVBERi0xLjQKJcTl8uXr...`. |
| `fileFromContentName` | string | no | Example: `contract.pdf`. |
| `sendReminders` | boolean | no |  |
| `template` | string | no | Example: `https://signrequest.com/api/v1/templates/<uuid>/`. |
| `externalId` | string | no | Example: `crm-doc-123`. |
| `eventsCallbackUrl` | string | no | Example: `https://example.com/signrequest/events`. |
| `autoDeleteDays` | number | no |  |
| `autoExpireDays` | number | no |  |
| `frontendId` | string | no | Example: `frontend-access-token`. |
| `fileFromSf` | object | no |  |
| `prefillTags[]` | array<object> | no |  |
| `integrations[]` | array<object> | no |  |
| `fromEmailName` | string | no | Example: `Legal Team`. |
| `isBeingPrepared` | boolean | no |  |
| `redirectUrl` | string | no | Example: `https://example.com/signed`. |
| `redirectUrlDeclined` | string | no | Example: `https://example.com/declined`. |
| `requiredAttachments[]` | array<object> | no |  |
| `disableAttachments` | boolean | no |  |
| `disableTextSignatures` | boolean | no |  |
| `disableText` | boolean | no |  |
| `disableDate` | boolean | no |  |
| `disableUploadSignatures` | boolean | no |  |
| `forceSignatureColor` | string | no | Example: `blue`. |
| `disableBlockchainProof` | boolean | no |  |
| `textMessageVerificationLocked` | boolean | no |  |
| `integration` | list<string> | no | One of: `formdesk`, `mfiles`, `microsoft-flow`, `salesforce`, `zapier`. |
| `integrationData` | object | no |  |
| `signers[].firstName` | string | no | Example: `Taylor`. |
| `signers[].lastName` | string | no | Example: `Jordan`. |
| `signers[].order` | number | no |  |
| `signers[].language` | list<string> | no | One of: `da`, `de`, `en`, `en-gb`, `es`, `fi`, `fr`, `he`, `hu`, `it`, `ja`, `nl`, `no`, `pl`, `pt`, `ru`, `sv`. |
| `signers[].forceLanguage` | boolean | no |  |
| `signers[].needsToSign` | boolean | no |  |
| `signers[].approveOnly` | boolean | no |  |
| `signers[].notifyOnly` | boolean | no |  |
| `signers[].inPerson` | boolean | no |  |
| `signers[].password` | string | no | Example: `signer-password`. |
| `signers[].verifyPhoneNumber` | string | no | Example: `+15551234567`. |
| `signers[].verifyBankAccount` | string | no | Example: `NL00BANK0123456789`. |
| `signers[].redirectUrl` | string | no | Example: `https://example.com/signed`. |
| `signers[].redirectUrlDeclined` | string | no | Example: `https://example.com/declined`. |
| `signers[].afterDocument` | string | no | Example: `https://signrequest.com/api/v1/documents/45bce8eb-0ab1-4e9f-a40a-eea49018c568/`. |
| `signers[].useStampForApproveOnly` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoDeleteDays": 1,
      "autoExpireDays": 1,
      "disableAttachments": true,
      "disableBlockchainProof": true,
      "disableDate": true,
      "disableEmails": true,
      "disableText": true,
      "disableTextSignatures": true,
      "disableUploadSignatures": true,
      "document": "string",
      "eventsCallbackUrl": "https://example.com",
      "externalId": "string",
      "file": "string",
      "fileFromSf": {},
      "fileFromUrl": "https://example.com",
      "forceSignatureColor": "string",
      "fromEmail": "ava@example.com",
      "fromEmailName": "ava@example.com",
      "integration": "string",
      "integrationData": {},
      "isBeingPrepared": true,
      "message": "string",
      "name": "Ava Chen",
      "prepareUrl": "https://example.com",
      "redirectUrl": "https://example.com",
      "redirectUrlDeclined": "https://example.com",
      "requiredAttachments": [
        [
          {}
        ]
      ],
      "sendReminders": true,
      "signers": [
        [
          {}
        ]
      ],
      "subject": "string",
      "textMessageVerificationLocked": true,
      "url": "https://example.com",
      "uuid": "string",
      "who": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoDeleteDays` | number |  |
| `autoExpireDays` | number |  |
| `disableAttachments` | boolean |  |
| `disableBlockchainProof` | boolean |  |
| `disableDate` | boolean |  |
| `disableEmails` | boolean |  |
| `disableText` | boolean |  |
| `disableTextSignatures` | boolean |  |
| `disableUploadSignatures` | boolean |  |
| `document` | string |  |
| `eventsCallbackUrl` | string |  |
| `externalId` | string |  |
| `file` | string |  |
| `fileFromSf` | object |  |
| `fileFromUrl` | string |  |
| `forceSignatureColor` | string |  |
| `fromEmail` | string |  |
| `fromEmailName` | string |  |
| `integration` | string |  |
| `integrationData` | object |  |
| `isBeingPrepared` | boolean |  |
| `message` | string |  |
| `name` | string |  |
| `prepareUrl` | string |  |
| `redirectUrl` | string |  |
| `redirectUrlDeclined` | string |  |
| `requiredAttachments[]` | array<object> |  |
| `sendReminders` | boolean |  |
| `signers[]` | array<object> |  |
| `signers[].afterDocument` | string |  |
| `signers[].approveOnly` | boolean |  |
| `signers[].attachments[]` | array<object> |  |
| `signers[].declined` | boolean |  |
| `signers[].declinedOn` | date |  |
| `signers[].displayName` | string |  |
| `signers[].downloaded` | boolean |  |
| `signers[].email` | string |  |
| `signers[].emailed` | boolean |  |
| `signers[].emailViewed` | boolean |  |
| `signers[].embedUrl` | string |  |
| `signers[].embedUrlUserId` | string |  |
| `signers[].firstName` | string |  |
| `signers[].forceLanguage` | boolean |  |
| `signers[].forwarded` | boolean |  |
| `signers[].forwardedOn` | date |  |
| `signers[].forwardedReason` | string |  |
| `signers[].forwardedToEmail` | string |  |
| `signers[].inPerson` | boolean |  |
| `signers[].inputs[]` | array<object> |  |
| `signers[].integrations[]` | array<object> |  |
| `signers[].language` | string |  |
| `signers[].lastName` | string |  |
| `signers[].message` | string |  |
| `signers[].needsToSign` | boolean |  |
| `signers[].notifyOnly` | boolean |  |
| `signers[].order` | number |  |
| `signers[].redirectUrl` | string |  |
| `signers[].redirectUrlDeclined` | string |  |
| `signers[].signed` | boolean |  |
| `signers[].signedOn` | date |  |
| `signers[].useStampForApproveOnly` | boolean |  |
| `signers[].verifyBankAccount` | string |  |
| `signers[].verifyPhoneNumber` | string |  |
| `signers[].viewed` | boolean |  |
| `subject` | string |  |
| `textMessageVerificationLocked` | boolean |  |
| `url` | string |  |
| `uuid` | string |  |
| `who` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `POST /signrequest-quick-create/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/quick-create-sign-request.md) for the provider-specific parameters and requirements.

