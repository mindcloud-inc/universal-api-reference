# Dropbox Sign: Send Signature Request

Creates a signature request in Dropbox Sign.

```
POST https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/send-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/send-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signers[].email_address": "ava@example.com",
  "signers[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/send-signature-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signers[].email_address": "ava@example.com",
    "signers[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_urls[]` | array<string> | no | One or more public file URLs for Dropbox Sign to fetch. Use this or uploaded files, not both. |
| `message` | string | no | The email message sent to signers. |
| `signers[].email_address` | string | yes | The email address of the signer. |
| `signers[].name` | string | yes | The name of the signer. |
| `subject` | string | no | The email subject sent to signers. |
| `test_mode` | boolean | no | Whether to create the signature request in test mode. |
| `title` | string | no | The title to assign to the signature request. |
| `use_text_tags` | boolean | no | Whether to enable Dropbox Sign text tag parsing in the document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "detailsUrl": "https://example.com",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "filesUrl": "https://example.com",
      "finalCopyUri": "string",
      "hasError": true,
      "isComplete": true,
      "isDeclined": true,
      "message": "string",
      "originalTitle": "string",
      "requesterEmailAddress": "ava@example.com",
      "signatureRequestId": "string",
      "signatures": [
        {
          "error": {},
          "hasPin": true,
          "hasSmsAuth": true,
          "hasSmsDelivery": true,
          "lastRemindedAt": "2026-05-07T12:00:00.000Z",
          "lastViewedAt": "2026-05-07T12:00:00.000Z",
          "order": {},
          "signatureId": "string",
          "signedAt": "2026-05-07T12:00:00.000Z",
          "signerEmailAddress": "ava@example.com",
          "signerName": "Ava Chen",
          "signerRole": {},
          "smsPhoneNumber": {},
          "statusCode": "string"
        }
      ],
      "signerExperience": {
        "formView": "string"
      },
      "signingRedirectUrl": {},
      "signingUrl": "https://example.com",
      "subject": "string",
      "templateIds": {},
      "testMode": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `detailsUrl` | string |  |
| `expiresAt` | date |  |
| `filesUrl` | string |  |
| `finalCopyUri` | string |  |
| `hasError` | boolean |  |
| `isComplete` | boolean |  |
| `isDeclined` | boolean |  |
| `message` | string |  |
| `originalTitle` | string |  |
| `requesterEmailAddress` | string |  |
| `signatureRequestId` | string |  |
| `signatures[].error` | object |  |
| `signatures[].hasPin` | boolean |  |
| `signatures[].hasSmsAuth` | boolean |  |
| `signatures[].hasSmsDelivery` | boolean |  |
| `signatures[].lastRemindedAt` | date |  |
| `signatures[].lastViewedAt` | date |  |
| `signatures[].order` | object |  |
| `signatures[].signatureId` | string |  |
| `signatures[].signedAt` | date |  |
| `signatures[].signerEmailAddress` | string |  |
| `signatures[].signerName` | string |  |
| `signatures[].signerRole` | object |  |
| `signatures[].smsPhoneNumber` | object |  |
| `signatures[].statusCode` | string |  |
| `signerExperience.formView` | string |  |
| `signingRedirectUrl` | object |  |
| `signingUrl` | string |  |
| `subject` | string |  |
| `templateIds` | object |  |
| `testMode` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Dropbox Sign API, this operation is `POST /signature_request/send` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-signature-request.md) for the provider-specific parameters and requirements.

