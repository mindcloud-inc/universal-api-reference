# Yousign: Create Signature Request

Creates a new signature request in Yousign.

```
POST https://connect.mindcloud.co/v1/universal/yousign/latest/actions/create-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/create-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "deliveryMode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yousign/latest/actions/create-signature-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "deliveryMode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Signature request name. |
| `deliveryMode` | string | yes | How Yousign should notify signers: email or none. |
| `orderedSigners` | boolean | no | Whether signers should be processed sequentially. |
| `workspaceId` | string | no | Workspace ID to scope the signature request. |
| `timezone` | string | no | Signature request timezone. |
| `expirationDate` | string | no | Due date in yyyy-mm-dd format. |
| `externalId` | string | no | External identifier to attach to the signature request. |
| `templateId` | string | no | Existing Yousign template ID to base the signature request on. |
| `signersAllowedToDecline` | boolean | no | Whether signers may decline to sign. |

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
      "bulkSendBatchId": {},
      "createdAt": "string",
      "customExperienceId": {},
      "customProperties": [
        [
          "string"
        ]
      ],
      "customRecipientOrder": true,
      "deliveryMode": "string",
      "documents": [
        [
          "string"
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
          "string"
        ]
      ],
      "signersAllowedToDecline": true,
      "source": "string",
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
| `bulkSendBatchId` | object |  |
| `createdAt` | string |  |
| `customExperienceId` | object |  |
| `customProperties[]` | array<string> |  |
| `customRecipientOrder` | boolean |  |
| `deliveryMode` | string |  |
| `documents[]` | array<string> |  |
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
| `signers[]` | array<string> |  |
| `signersAllowedToDecline` | boolean |  |
| `source` | string |  |
| `status` | string |  |
| `timezone` | string |  |
| `workflowSessionId` | object |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Yousign API, this operation is `POST /signature_requests` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signature-request.md) for the provider-specific parameters and requirements.

