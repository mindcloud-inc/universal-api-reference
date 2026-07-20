# Clockify: Create Time Off Policy

Creates a time off policy in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-time-off-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-time-off-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "approve": {},
  "name": "Example Name",
  "automaticAccrual.amount": 1,
  "automaticTimeEntryCreation.defaultEntities": {},
  "negativeBalance.amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-time-off-policy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "approve": {},
    "name": "Example Name",
    "automaticAccrual.amount": 1,
    "automaticTimeEntryCreation.defaultEntities": {},
    "negativeBalance.amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `approve` | object | yes |  |
| `name` | string | yes | Example: `Example Name`. |
| `allowHalfDay` | boolean | no | Example: `true`. |
| `allowNegativeBalance` | boolean | no | Example: `true`. |
| `archived` | boolean | no | Example: `true`. |
| `automaticAccrual` | object | no |  |
| `automaticTimeEntryCreation` | object | no |  |
| `color` | string | no |  |
| `everyoneIncludingNew` | boolean | no | Example: `true`. |
| `hasExpiration` | boolean | no | Example: `true`. |
| `icon` | list<string> | no | One of: `CALENDAR`, `CHILDCARE`, `FAMILY`, `HEALTH_METRICS`, `LUGGAGE`, `MONETIZATION`, `PLANE`, `SNOWFLAKE`, `STETHOSCOPE`, `UMBRELLA`. |
| `negativeBalance` | object | no |  |
| `timeUnit` | list<string> | no | One of: `DAYS`, `HOURS`. Example: `2026-01-01T09:00:00Z`. |
| `userGroups` | object | no |  |
| `users` | object | no |  |
| `approve.requiresApproval` | boolean | no |  |
| `approve.specificMembers` | boolean | no |  |
| `approve.teamManagers` | boolean | no |  |
| `approve.userIds[]` | array<string> | no |  |
| `automaticAccrual.amount` | number | yes |  |
| `automaticAccrual.period` | string | no |  |
| `automaticAccrual.timeUnit` | string | no |  |
| `automaticTimeEntryCreation.defaultEntities` | object | yes |  |
| `automaticTimeEntryCreation.defaultEntities.projectId` | string | no |  |
| `automaticTimeEntryCreation.defaultEntities.taskId` | string | no |  |
| `automaticTimeEntryCreation.enabled` | boolean | no |  |
| `negativeBalance.amount` | number | yes |  |
| `negativeBalance.amountValidForTimeUnit` | boolean | no |  |
| `negativeBalance.period` | string | no |  |
| `negativeBalance.shouldReset` | boolean | no |  |
| `negativeBalance.timeUnit` | string | no |  |
| `userGroups.contains` | string | no |  |
| `userGroups.ids[]` | array<string> | no |  |
| `userGroups.status` | string | no |  |
| `users.contains` | string | no |  |
| `users.ids[]` | array<string> | no |  |
| `users.status` | string | no |  |

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

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/time-off/policies` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-off-policy.md) for the provider-specific parameters and requirements.

