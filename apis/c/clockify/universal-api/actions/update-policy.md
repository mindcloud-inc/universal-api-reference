# Clockify: Update Policy

Updates an existing policy in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "id": "string",
  "allowHalfDay": "true",
  "allowNegativeBalance": "true",
  "approve": {},
  "archived": "true",
  "everyoneIncludingNew": "true",
  "hasExpiration": "true",
  "name": "Example Name",
  "userGroups": {},
  "users": {},
  "automaticAccrual.amount": 1,
  "automaticTimeEntryCreation.defaultEntities": {},
  "negativeBalance.amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-policy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "id": "string",
    "allowHalfDay": "true",
    "allowNegativeBalance": "true",
    "approve": {},
    "archived": "true",
    "everyoneIncludingNew": "true",
    "hasExpiration": "true",
    "name": "Example Name",
    "userGroups": {},
    "users": {},
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
| `id` | string<string> | yes |  |
| `allowHalfDay` | boolean | yes | Example: `true`. |
| `allowNegativeBalance` | boolean | yes | Example: `true`. |
| `approve` | object | yes |  |
| `archived` | boolean | yes | Example: `true`. |
| `everyoneIncludingNew` | boolean | yes | Example: `true`. |
| `hasExpiration` | boolean | yes | Example: `true`. |
| `name` | string | yes | Example: `Example Name`. |
| `userGroups` | object | yes |  |
| `users` | object | yes |  |
| `automaticAccrual` | object | no |  |
| `automaticTimeEntryCreation` | object | no |  |
| `color` | string | no |  |
| `icon` | list<string> | no | One of: `CALENDAR`, `CHILDCARE`, `FAMILY`, `HEALTH_METRICS`, `LUGGAGE`, `MONETIZATION`, `PLANE`, `SNOWFLAKE`, `STETHOSCOPE`, `UMBRELLA`. |
| `negativeBalance` | object | no |  |
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

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/time-off/policies/:id` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-policy.md) for the provider-specific parameters and requirements.

