# Yousign: Cancel Signature Request

Cancels a signature request in Yousign.

```
PUT https://connect.mindcloud.co/v1/universal/yousign/latest/actions/cancel-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/cancel-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string",
  "reason": "contractualization_aborted"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yousign/latest/actions/cancel-signature-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string",
    "reason": "contractualization_aborted"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | The Yousign signature request ID. |
| `reason` | list<string> | yes | Cancellation reason. One of: `contractualization_aborted`, `errors_in_document`, `other`. |
| `customNote` | string | no | Optional cancellation note. |

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
| `signers[].customText` | object |  |
| `signers[].customText.reminderBody` | object |  |
| `signers[].customText.reminderSubject` | object |  |
| `signers[].customText.requestBody` | object |  |
| `signers[].customText.requestSubject` | object |  |
| `signers[].deliveryMode` | string |  |
| `signers[].id` | string |  |
| `signers[].status` | string |  |
| `signersAllowedToDecline` | boolean |  |
| `source` | string |  |
| `status` | string |  |
| `timezone` | string |  |
| `workflowSessionId` | object |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Yousign API, this operation is `POST /signature_requests/:signatureRequestId/cancel` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-signature-request.md) for the provider-specific parameters and requirements.

