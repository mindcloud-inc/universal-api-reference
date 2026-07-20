# Clockify: Change Policy Status

Updates a policy status in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/change-policy-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/change-policy-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "id": "string",
  "status": "ACTIVE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/change-policy-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "id": "string",
    "status": "ACTIVE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `id` | string<string> | yes |  |
| `status` | list<string> | yes | One of: `ACTIVE`, `ALL`, `ARCHIVED`. Example: `ACTIVE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowHalfDay": true,
      "allowNegativeBalance": true,
      "approve": {
        "requiresApproval": true,
        "specificMembers": true,
        "teamManagers": true,
        "userIds": [
          [
            "string"
          ]
        ]
      },
      "archived": true,
      "automaticAccrual": {
        "amount": 1,
        "period": "string",
        "timeUnit": "string"
      },
      "automaticTimeEntryCreation": {
        "defaultEntities": {
          "projectId": "string",
          "taskId": "string"
        },
        "enabled": true
      },
      "everyoneIncludingNew": true,
      "id": "string",
      "name": "Ava Chen",
      "negativeBalance": {
        "amount": 1,
        "period": "string",
        "shouldReset": true,
        "timeUnit": "string"
      },
      "projectId": "string",
      "timeUnit": "string",
      "userGroupIds": [
        [
          "string"
        ]
      ],
      "userIds": [
        [
          "string"
        ]
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowHalfDay` | boolean |  |
| `allowNegativeBalance` | boolean |  |
| `approve` | object |  |
| `approve.requiresApproval` | boolean |  |
| `approve.specificMembers` | boolean |  |
| `approve.teamManagers` | boolean |  |
| `approve.userIds[]` | array<string> |  |
| `archived` | boolean |  |
| `automaticAccrual` | object |  |
| `automaticAccrual.amount` | number |  |
| `automaticAccrual.period` | string |  |
| `automaticAccrual.timeUnit` | string |  |
| `automaticTimeEntryCreation` | object |  |
| `automaticTimeEntryCreation.defaultEntities` | object |  |
| `automaticTimeEntryCreation.defaultEntities.projectId` | string |  |
| `automaticTimeEntryCreation.defaultEntities.taskId` | string |  |
| `automaticTimeEntryCreation.enabled` | boolean |  |
| `everyoneIncludingNew` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `negativeBalance` | object |  |
| `negativeBalance.amount` | number |  |
| `negativeBalance.period` | string |  |
| `negativeBalance.shouldReset` | boolean |  |
| `negativeBalance.timeUnit` | string |  |
| `projectId` | string |  |
| `timeUnit` | string |  |
| `userGroupIds[]` | array<string> |  |
| `userIds[]` | array<string> |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `PATCH workspaces/:workspaceId/time-off/policies/:id` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-policy-status.md) for the provider-specific parameters and requirements.

