# WebWork Time Tracker: Get Project

Retrieves a project from WebWork Time Tracker.

```
GET https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=1&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-project?${params}`, {
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
| `projectId` | number | yes |  |
| `workspaceId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "budgetEstimation": 1,
      "contractsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deadline": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "estimation": 1,
      "icon": "string",
      "id": 1,
      "isBillable": true,
      "name": "Ava Chen",
      "notes": "string",
      "ownerId": 1,
      "rate": 1,
      "screenshots": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "weeklyHoursLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budgetEstimation` | number |  |
| `contractsCount` | number |  |
| `createdAt` | date |  |
| `deadline` | date |  |
| `deletedAt` | date |  |
| `estimation` | number |  |
| `icon` | string |  |
| `id` | number |  |
| `isBillable` | boolean |  |
| `name` | string |  |
| `notes` | string |  |
| `ownerId` | number |  |
| `rate` | number |  |
| `screenshots` | string |  |
| `startDate` | date |  |
| `status` | number |  |
| `updatedAt` | date |  |
| `weeklyHoursLimit` | number |  |

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `GET /projects/:projectId` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

