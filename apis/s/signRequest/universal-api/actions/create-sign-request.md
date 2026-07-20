# SignRequest: Create SignRequest



```
POST https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-sign-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-sign-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "https://signrequest.com/api/v1/documents/<uuid>/",
  "signers[]": [
    {}
  ],
  "signers[].email": "signer@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-sign-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "https://signrequest.com/api/v1/documents/<uuid>/",
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
| `document` | string | yes | Document URL returned by the SignRequest documents API Example: `https://signrequest.com/api/v1/documents/<uuid>/`. |
| `signers[]` | array<object> | yes | Signers to include on the SignRequest |
| `signers[].email` | string | yes | Signer email address Example: `signer@example.com`. |
| `fromEmail` | string | no | Validated email address of the user sending the SignRequest Example: `you@example.com`. |
| `subject` | string | no | Subject of the SignRequest email Example: `Please sign this agreement`. |
| `message` | string | no | Message to include in the SignRequest email Example: `Please review and sign this document.`. |
| `who` | list<string> | no | Who needs to sign: only me, me and others, or only others One of: `m`, `mo`, `o`. |
| `disableEmails` | boolean | no | Disable SignRequest status emails and signed-document emails Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendReminders` | boolean | no | Automatically remind signers to sign |
| `fromEmailName` | string | no | Name used in the From email header Example: `Alex from Legal`. |
| `signers[].firstName` | string | no | Signer first name Example: `Taylor`. |
| `signers[].lastName` | string | no | Signer last name Example: `Smith`. |
| `signers[].order` | number | no | Signer order in the signing flow Example: `0`. |
| `signers[].language` | list<string> | no | Signer language One of: `da`, `de`, `en`, `en-gb`, `es`, `fi`, `fr`, `he`, `hu`, `it`, `ja`, `nl`, `no`, `pl`, `pt`, `ru`, `sv`. |
| `signers[].forceLanguage` | boolean | no | Force the selected signer language |
| `signers[].needsToSign` | boolean | no | Whether the signer must sign the document |
| `signers[].approveOnly` | boolean | no | Require approval without adding a signature |
| `signers[].notifyOnly` | boolean | no | Notify the signer without requiring action |
| `signers[].inPerson` | boolean | no | Use in-person signing for this signer |
| `signers[].password` | string | no | Password the signer must enter before signing Example: `s3cur3-passphrase`. |
| `signers[].verifyPhoneNumber` | string | no | Phone number required for signer verification Example: `+15551234567`. |
| `signers[].verifyBankAccount` | string | no | Bank account required for signer verification Example: `NL00BANK0123456789`. |
| `signers[].redirectUrl` | string | no | Signer-specific redirect URL after signing Example: `https://example.com/signed`. |
| `signers[].redirectUrlDeclined` | string | no | Signer-specific redirect URL after declining Example: `https://example.com/declined`. |
| `signers[].afterDocument` | string | no | Document URL that should be signed before this signer Example: `https://signrequest.com/api/v1/documents/<uuid>/`. |
| `signers[].useStampForApproveOnly` | boolean | no | Place an approval stamp when a signer approves the document |
| `redirectUrl` | string | no | Redirect users here after signing Example: `https://example.com/signed`. |
| `redirectUrlDeclined` | string | no | Redirect users here after declining Example: `https://example.com/declined`. |
| `isBeingPrepared` | boolean | no | Have the sender prepare the document before sending |
| `requiredAttachments[]` | array<object> | no | Attachments that signers are required to upload |
| `disableAttachments` | boolean | no | Disable uploading or adding attachments |
| `disableTextSignatures` | boolean | no | Disable typed text signatures |
| `disableText` | boolean | no | Disable adding text |
| `disableDate` | boolean | no | Disable adding dates |
| `disableUploadSignatures` | boolean | no | Disable uploaded image signatures |
| `forceSignatureColor` | string | no | Force a specific signature color Example: `blue`. |
| `disableBlockchainProof` | boolean | no | Disable storing timestamp proof hashes in blockchain integrations |
| `textMessageVerificationLocked` | boolean | no | Require text message verification before the signer can view the document |
| `integration` | list<string> | no | Integration identifier for the SignRequest record One of: `formdesk`, `mfiles`, `microsoft-flow`, `salesforce`, `zapier`. |
| `integrationData` | object | no | Integration-specific payload for the SignRequest |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disableAttachments": true,
      "disableBlockchainProof": true,
      "disableDate": true,
      "disableEmails": true,
      "disableText": true,
      "disableTextSignatures": true,
      "disableUploadSignatures": true,
      "document": "string",
      "forceSignatureColor": "string",
      "fromEmail": "ava@example.com",
      "fromEmailName": "ava@example.com",
      "integration": "string",
      "integrationData": {},
      "isBeingPrepared": true,
      "message": "string",
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
| `disableAttachments` | boolean |  |
| `disableBlockchainProof` | boolean |  |
| `disableDate` | boolean |  |
| `disableEmails` | boolean |  |
| `disableText` | boolean |  |
| `disableTextSignatures` | boolean |  |
| `disableUploadSignatures` | boolean |  |
| `document` | string |  |
| `forceSignatureColor` | string |  |
| `fromEmail` | string |  |
| `fromEmailName` | string |  |
| `integration` | string |  |
| `integrationData` | object |  |
| `isBeingPrepared` | boolean |  |
| `message` | string |  |
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

Through the native SignRequest API, this operation is `POST /signrequests/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sign-request.md) for the provider-specific parameters and requirements.

