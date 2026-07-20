# Yousign: Add Signature Request Signer

Creates a signer for a Yousign signature request.

```
POST https://connect.mindcloud.co/v1/universal/yousign/latest/actions/add-signature-request-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/add-signature-request-signer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string",
  "contactId": "string",
  "signatureLevel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yousign/latest/actions/add-signature-request-signer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string",
    "contactId": "string",
    "signatureLevel": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | The Yousign signature request ID. |
| `contactId` | string | yes | Existing contact to add as signer. |
| `signatureLevel` | string | yes | Signer signature level. |
| `signatureAuthenticationMode` | string | no | Signer authentication mode. |
| `deliveryMode` | string | no | Signer delivery mode. |
| `insertAfterId` | string | no | Recipient ID this signer should follow. |
| `groupWithId` | string | no | Recipient ID to group with. |
| `redirectUrls.success` | string | no | Redirect URL on successful signature. |
| `redirectUrls.error` | string | no | Redirect URL on signature error. |
| `redirectUrls.decline` | string | no | Redirect URL on signature decline. |
| `identificationAttestationId` | string | no | Identification attestation ID, when required. |
| `preIdentityVerificationRequired` | boolean | no | Require identity verification before signing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customText": {
        "reminderBody": {},
        "reminderSubject": {},
        "requestBody": {},
        "requestSubject": {}
      },
      "deliveryMode": "string",
      "emailNotification": {
        "disabled": [
          [
            "ava@example.com"
          ]
        ]
      },
      "fields": {},
      "id": "string",
      "identificationAttestationId": {},
      "info": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "locale": "string",
        "phoneNumber": "string"
      },
      "preIdentityVerificationRequired": true,
      "recipientStageIndex": 1,
      "redirectUrls": {
        "decline": {},
        "error": {},
        "success": {}
      },
      "signatureAuthenticationMode": "string",
      "signatureImagePreview": "string",
      "signatureLevel": "string",
      "signatureLink": {},
      "signatureLinkExpirationDate": {},
      "smsNotification": {
        "otpMessage": {
          "customText": {}
        }
      },
      "status": "string",
      "verifiedIdentityId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customText` | object |  |
| `customText.reminderBody` | object |  |
| `customText.reminderSubject` | object |  |
| `customText.requestBody` | object |  |
| `customText.requestSubject` | object |  |
| `deliveryMode` | string |  |
| `emailNotification` | object |  |
| `emailNotification.disabled[]` | array<string> |  |
| `fields` | object |  |
| `id` | string |  |
| `identificationAttestationId` | object |  |
| `info` | object |  |
| `info.email` | string |  |
| `info.firstName` | string |  |
| `info.lastName` | string |  |
| `info.locale` | string |  |
| `info.phoneNumber` | string |  |
| `preIdentityVerificationRequired` | boolean |  |
| `recipientStageIndex` | number |  |
| `redirectUrls` | object |  |
| `redirectUrls.decline` | object |  |
| `redirectUrls.error` | object |  |
| `redirectUrls.success` | object |  |
| `signatureAuthenticationMode` | string |  |
| `signatureImagePreview` | string |  |
| `signatureLevel` | string |  |
| `signatureLink` | object |  |
| `signatureLinkExpirationDate` | object |  |
| `smsNotification` | object |  |
| `smsNotification.otpMessage` | object |  |
| `smsNotification.otpMessage.customText` | object |  |
| `status` | string |  |
| `verifiedIdentityId` | object |  |

## Native endpoint

Through the native Yousign API, this operation is `POST /signature_requests/:signatureRequestId/signers` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-signature-request-signer.md) for the provider-specific parameters and requirements.

