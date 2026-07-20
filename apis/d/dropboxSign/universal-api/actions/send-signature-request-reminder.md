# Dropbox Sign: Send Signature Request Reminder

Sends a signature request reminder in Dropbox Sign.

```
PUT https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/send-signature-request-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/send-signature-request-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "ava@example.com",
  "signature_request_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/send-signature-request-reminder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "ava@example.com",
    "signature_request_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | yes | The email address of the signer to send a reminder to. |
| `name` | string | no | The signer name. Include it if two or more signers share an email address. |
| `signature_request_id` | string | yes | The id of the SignatureRequest to send a reminder for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {
          "apiId": "string",
          "editor": {},
          "name": "Ava Chen",
          "required": true,
          "type": "string",
          "value": "string"
        }
      ],
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
| `customFields[].apiId` | string |  |
| `customFields[].editor` | object |  |
| `customFields[].name` | string |  |
| `customFields[].required` | boolean |  |
| `customFields[].type` | string |  |
| `customFields[].value` | string |  |
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

Through the native Dropbox Sign API, this operation is `POST /signature_request/remind/:signature_request_id` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-signature-request-reminder.md) for the provider-specific parameters and requirements.

