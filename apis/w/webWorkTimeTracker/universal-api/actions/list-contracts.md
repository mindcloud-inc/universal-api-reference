# WebWork Time Tracker: List Contracts

Retrieves workspace contracts from WebWork Time Tracker.

```
GET https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-contracts?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-contracts?${params}`, {
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
| `workspaceId` | number | yes |  |
| `projectId` | number | no |  |
| `userId` | number | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contractName": "Ava Chen",
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
| `contractName` | string |  |
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

Through the native WebWork Time Tracker API, this operation is `GET /contracts` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contracts.md) for the provider-specific parameters and requirements.

