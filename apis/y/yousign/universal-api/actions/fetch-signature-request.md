# Yousign: Fetch Signature Request

Retrieves a signature request from Yousign.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/fetch-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/fetch-signature-request?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/fetch-signature-request?${params}`, {
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
      "declineInformation": {},
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
| `declineInformation` | object |  |
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

Through the native Yousign API, this operation is `GET /signature_requests/:signatureRequestId` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-signature-request.md) for the provider-specific parameters and requirements.

