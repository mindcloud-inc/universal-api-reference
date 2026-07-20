# SignRequest: List SignRequests



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-sign-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-sign-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-sign-requests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `who` | list<string> | no | `m`: only me, `mo`: me and others, `o`: only others. One of: `m`, `mo`, `o`. |
| `fromEmail` | string | no | Example: `you@example.com`. |

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

Through the native SignRequest API, this operation is `GET /signrequests/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sign-requests.md) for the provider-specific parameters and requirements.

