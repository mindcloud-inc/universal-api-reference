# Yousign: Activate Signature Request

Activates a signature request in Yousign.

```
PUT https://connect.mindcloud.co/v1/universal/yousign/latest/actions/activate-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/activate-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yousign/latest/actions/activate-signature-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | The Yousign signature request ID. |
| `senderId` | string | no | Optional user ID to act as the sender during activation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvers": [
        [
          "string"
        ]
      ],
      "auditTrailLocale": "string",
      "brandingId": {},
      "createdAt": "string",
      "customExperienceId": {},
      "customRecipientOrder": true,
      "deliveryMode": "string",
      "documents": [
        [
          {}
        ]
      ],
      "emailCustomNote": {},
      "emailNotification": {
        "customNote": {},
        "customText": {
          "reminderBody": {},
          "reminderSubject": {},
          "requestBody": {},
          "requestSubject": {}
        },
        "sender": {
          "customName": {},
          "type": "ava@example.com"
        }
      },
      "expirationDate": "string",
      "externalId": "string",
      "id": "string",
      "labels": [
        [
          "string"
        ]
      ],
      "name": "Ava Chen",
      "orderedApprovers": true,
      "orderedSigners": true,
      "previousAttemptId": {},
      "rejectionInformation": {},
      "reminderSettings": {},
      "sender": {},
      "signers": [
        [
          {}
        ]
      ],
      "signersAllowedToDecline": true,
      "status": "string",
      "timezone": "string",
      "workflowSessionId": {},
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvers[]` | array<string> |  |
| `auditTrailLocale` | string |  |
| `brandingId` | object |  |
| `createdAt` | string |  |
| `customExperienceId` | object |  |
| `customRecipientOrder` | boolean |  |
| `deliveryMode` | string |  |
| `documents[]` | array<object> |  |
| `documents[].id` | string |  |
| `documents[].nature` | string |  |
| `emailCustomNote` | object |  |
| `emailNotification` | object |  |
| `emailNotification.customNote` | object |  |
| `emailNotification.customText` | object |  |
| `emailNotification.customText.reminderBody` | object |  |
| `emailNotification.customText.reminderSubject` | object |  |
| `emailNotification.customText.requestBody` | object |  |
| `emailNotification.customText.requestSubject` | object |  |
| `emailNotification.sender` | object |  |
| `emailNotification.sender.customName` | object |  |
| `emailNotification.sender.type` | string |  |
| `expirationDate` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `labels[]` | array<string> |  |
| `name` | string |  |
| `orderedApprovers` | boolean |  |
| `orderedSigners` | boolean |  |
| `previousAttemptId` | object |  |
| `rejectionInformation` | object |  |
| `reminderSettings` | object |  |
| `sender` | object |  |
| `signers[]` | array<object> |  |
| `signers[].deliveryMode` | string |  |
| `signers[].id` | string |  |
| `signers[].signatureLink` | string |  |
| `signers[].signatureLinkExpirationDate` | string |  |
| `signers[].status` | string |  |
| `signersAllowedToDecline` | boolean |  |
| `status` | string |  |
| `timezone` | string |  |
| `workflowSessionId` | object |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Yousign API, this operation is `POST /signature_requests/:signatureRequestId/activate` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-signature-request.md) for the provider-specific parameters and requirements.

