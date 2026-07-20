# Clockify: Update Task Cost Rate

Updates a task cost rate in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-task-cost-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-task-cost-rate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "projectId": "string",
  "id": "string",
  "amount": "100"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-task-cost-rate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "projectId": "string",
    "id": "string",
    "amount": "100"
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
| `id` | string<string> | yes |  |
| `amount` | number | yes | Example: `100`. |
| `since` | string | no | Example: `2026-01-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "assigneeIds": [
        [
          "string"
        ]
      ],
      "billable": true,
      "budgetEstimate": 1,
      "costRate": {
        "amount": 1,
        "currency": "string"
      },
      "duration": "string",
      "estimate": "string",
      "hourlyRate": {
        "amount": 1,
        "currency": "https://example.com"
      },
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "status": "string",
      "userGroupIds": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | string |  |
| `assigneeIds[]` | array<string> |  |
| `billable` | boolean |  |
| `budgetEstimate` | number |  |
| `costRate` | object |  |
| `costRate.amount` | number |  |
| `costRate.currency` | string |  |
| `duration` | string |  |
| `estimate` | string |  |
| `hourlyRate` | object |  |
| `hourlyRate.amount` | number |  |
| `hourlyRate.currency` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `userGroupIds[]` | array<string> |  |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/projects/:projectId/tasks/:id/cost-rate` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-cost-rate.md) for the provider-specific parameters and requirements.

