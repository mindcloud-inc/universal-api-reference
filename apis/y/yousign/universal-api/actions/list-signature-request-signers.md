# Yousign: List Signature Request Signers

Retrieves signers from a Yousign signature request.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-request-signers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-request-signers?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-request-signers?${params}`, {
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
| `signatureRequestId` | string | yes | The Yousign signature request ID. |

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

Through the native Yousign API, this operation is `GET /signature_requests/:signatureRequestId/signers` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-request-signers.md) for the provider-specific parameters and requirements.

