# WebWork Time Tracker: Create Contract

Creates a new contract in WebWork Time Tracker.

```
POST https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/create-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/create-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "projectId": 1,
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/create-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "projectId": 1,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes |  |
| `projectId` | number | yes |  |
| `userId` | number | yes |  |
| `weeklyHoursLimit` | number | no |  |
| `screenshots` | string | no |  |
| `rate` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": 1,
      "projectIcon": "string",
      "projectId": 1,
      "projectName": "Ava Chen",
      "rate": 1,
      "rateType": 1,
      "screenshots": "string",
      "screenshotsLabel": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userEmail": "ava@example.com",
      "userFirstname": "Ava",
      "userId": 1,
      "userLastname": "Chen",
      "userRole": "string",
      "weeklyHoursLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `currency` | string |  |
| `id` | number |  |
| `projectIcon` | string |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `rate` | number |  |
| `rateType` | number |  |
| `screenshots` | string |  |
| `screenshotsLabel` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `userEmail` | string |  |
| `userFirstname` | string |  |
| `userId` | number |  |
| `userLastname` | string |  |
| `userRole` | string |  |
| `weeklyHoursLimit` | number |  |

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `POST /contracts` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract.md) for the provider-specific parameters and requirements.

