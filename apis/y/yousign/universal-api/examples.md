# Yousign Universal API Examples

These examples use the MindCloud API key and Yousign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Default Workspace

Retrieves the default workspace from Yousign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-default-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-default-workspace?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "externalName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        {
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Default Workspace action reference](actions/get-default-workspace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yousign/latest/actions/get-default-workspace).

## Activate Signature Request

Activates a signature request in Yousign.

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

Example response:

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

See the full [Activate Signature Request action reference](actions/activate-signature-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yousign/latest/actions/activate-signature-request).
