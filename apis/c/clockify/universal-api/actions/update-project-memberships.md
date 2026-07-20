# Clockify: Update Project Memberships

Updates workspace project memberships in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-project-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-project-memberships" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "projectId": "string",
  "memberships[]": [
    {}
  ],
  "memberships[].costRate.amount": 1,
  "memberships[].hourlyRate.amount": 1,
  "memberships[].userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-project-memberships', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "projectId": "string",
    "memberships[]": [{}],
    "memberships[].costRate.amount": 1,
    "memberships[].hourlyRate.amount": 1,
    "memberships[].userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `projectId` | string<string> | yes |  |
| `memberships[]` | array<object> | yes |  |
| `userGroups` | object | no |  |
| `memberships[].costRate` | object | no |  |
| `memberships[].costRate.amount` | number | yes |  |
| `memberships[].costRate.since` | string | no |  |
| `memberships[].hourlyRate` | object | no |  |
| `memberships[].hourlyRate.amount` | number | yes |  |
| `memberships[].hourlyRate.since` | string | no |  |
| `memberships[].userId` | string | yes |  |
| `userGroups.contains` | string | no |  |
| `userGroups.ids[]` | array<string> | no |  |
| `userGroups.status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "billable": true,
      "budgetEstimate": {
        "active": true,
        "estimate": 1,
        "includeExpenses": true,
        "resetOption": "string",
        "type": "string"
      },
      "clientId": "string",
      "clientName": "Ava Chen",
      "color": "string",
      "costRate": {
        "amount": 1,
        "currency": "string"
      },
      "duration": "string",
      "estimate": {
        "estimate": "string",
        "type": "string"
      },
      "estimateReset": {
        "dayOfMonth": 1,
        "dayOfWeek": "string",
        "hour": 1,
        "interval": "string",
        "month": "string"
      },
      "hourlyRate": {
        "amount": 1,
        "currency": "https://example.com"
      },
      "id": "string",
      "isPublic": true,
      "isTemplate": true,
      "memberships": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "note": "string",
      "public": true,
      "template": true,
      "timeEstimate": {
        "active": true,
        "estimate": "string",
        "includeNonBillable": true,
        "resetOption": "string",
        "type": "string"
      },
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `billable` | boolean |  |
| `budgetEstimate` | object |  |
| `budgetEstimate.active` | boolean |  |
| `budgetEstimate.estimate` | number |  |
| `budgetEstimate.includeExpenses` | boolean |  |
| `budgetEstimate.resetOption` | string |  |
| `budgetEstimate.type` | string |  |
| `clientId` | string |  |
| `clientName` | string |  |
| `color` | string |  |
| `costRate` | object |  |
| `costRate.amount` | number |  |
| `costRate.currency` | string |  |
| `duration` | string |  |
| `estimate` | object |  |
| `estimate.estimate` | string |  |
| `estimate.type` | string |  |
| `estimateReset` | object |  |
| `estimateReset.dayOfMonth` | number |  |
| `estimateReset.dayOfWeek` | string |  |
| `estimateReset.hour` | number |  |
| `estimateReset.interval` | string |  |
| `estimateReset.month` | string |  |
| `hourlyRate` | object |  |
| `hourlyRate.amount` | number |  |
| `hourlyRate.currency` | string |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `isTemplate` | boolean |  |
| `memberships[]` | array<object> |  |
| `memberships[].costRate` | object |  |
| `memberships[].costRate.amount` | number |  |
| `memberships[].costRate.currency` | string |  |
| `memberships[].hourlyRate` | object |  |
| `memberships[].hourlyRate.amount` | number |  |
| `memberships[].hourlyRate.currency` | string |  |
| `memberships[].membershipStatus` | string |  |
| `memberships[].membershipType` | string |  |
| `memberships[].targetId` | string |  |
| `memberships[].userId` | string |  |
| `name` | string |  |
| `note` | string |  |
| `public` | boolean |  |
| `template` | boolean |  |
| `timeEstimate` | object |  |
| `timeEstimate.active` | boolean |  |
| `timeEstimate.estimate` | string |  |
| `timeEstimate.includeNonBillable` | boolean |  |
| `timeEstimate.resetOption` | string |  |
| `timeEstimate.type` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `PATCH workspaces/:workspaceId/projects/:projectId/memberships` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-memberships.md) for the provider-specific parameters and requirements.

