# Clockify: Update Webhook

Updates an existing webhook in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "webhookId": "string",
  "triggerSource[]": [
    "string"
  ],
  "triggerSourceType": "STANDARD",
  "url": "https://example.com/webhook",
  "webhookEvent": "APPROVAL_REQUEST_STATUS_UPDATED"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "webhookId": "string",
    "triggerSource[]": ["string"],
    "triggerSourceType": "STANDARD",
    "url": "https://example.com/webhook",
    "webhookEvent": "APPROVAL_REQUEST_STATUS_UPDATED"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `webhookId` | string<string> | yes |  |
| `triggerSource[]` | array<string> | yes |  |
| `triggerSourceType` | list<string> | yes | One of: `ASSIGNMENT_ID`, `EXPENSE_ID`, `PROJECT_ID`, `TAG_ID`, `TASK_ID`, `USER_ID`, `WORKSPACE_ID`. Example: `STANDARD`. |
| `url` | string | yes | Example: `https://example.com/webhook`. |
| `webhookEvent` | list<string> | yes | One of: `APPROVAL_REQUEST_STATUS_UPDATED`, `ASSIGNMENT_CREATED`, `ASSIGNMENT_DELETED`, `ASSIGNMENT_PUBLISHED`, `ASSIGNMENT_UPDATED`, `BALANCE_UPDATED`, `BILLABLE_RATE_UPDATED`, `CLIENT_DELETED`, `CLIENT_UPDATED`, `COST_RATE_UPDATED`, `EXPENSE_CREATED`, `EXPENSE_DELETED`, `EXPENSE_RESTORED`, `EXPENSE_UPDATED`, `INVOICE_UPDATED`, `LIMITED_USERS_ADDED_TO_WORKSPACE`, `NEW_APPROVAL_REQUEST`, `NEW_CLIENT`, `NEW_INVOICE`, `NEW_PROJECT`, `NEW_TAG`, `NEW_TASK`, `NEW_TIMER_STARTED`, `NEW_TIME_ENTRY`, `PROJECT_DELETED`, `PROJECT_UPDATED`, `TAG_DELETED`, `TAG_UPDATED`, `TASK_DELETED`, `TASK_UPDATED`, `TIMER_STOPPED`, `TIME_ENTRY_DELETED`, `TIME_ENTRY_RESTORED`, `TIME_ENTRY_SPLIT`, `TIME_ENTRY_UPDATED`, `TIME_OFF_REQUESTED`, `TIME_OFF_REQUEST_APPROVED`, `TIME_OFF_REQUEST_REJECTED`, `TIME_OFF_REQUEST_UPDATED`, `TIME_OFF_REQUEST_WITHDRAWN`, `USERS_INVITED_TO_WORKSPACE`, `USER_ACTIVATED_ON_WORKSPACE`, `USER_DEACTIVATED_ON_WORKSPACE`, `USER_DELETED_FROM_WORKSPACE`, `USER_EMAIL_CHANGED`, `USER_GROUP_CREATED`, `USER_GROUP_DELETED`, `USER_GROUP_UPDATED`, `USER_JOINED_WORKSPACE`, `USER_UPDATED`. |
| `name` | string | no | Example: `Example Name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authToken": "string",
      "deliveryEnabled": true,
      "enabled": true,
      "id": "string",
      "name": "Ava Chen",
      "triggerSource": [
        [
          "string"
        ]
      ],
      "triggerSourceType": "string",
      "url": "https://example.com",
      "userId": "string",
      "webhookEvent": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authToken` | string |  |
| `deliveryEnabled` | boolean |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `triggerSource[]` | array<string> |  |
| `triggerSourceType` | string |  |
| `url` | string |  |
| `userId` | string |  |
| `webhookEvent` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/webhooks/:webhookId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

