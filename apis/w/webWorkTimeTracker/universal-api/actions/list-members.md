# WebWork Time Tracker: List Members

Retrieves workspace members from WebWork Time Tracker.

```
GET https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-members?${params}`, {
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
| `email` | string | no |  |
| `status` | string | no |  |
| `role` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentRole": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "isBlocked": true,
      "lastname": "Chen",
      "rate": 1,
      "rateStatus": 1,
      "rateType": "string",
      "screenshots": "string",
      "status": "string",
      "teamName": "Ava Chen",
      "timezone": "string",
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
| `avatar` | string |  |
| `createdAt` | date |  |
| `currentRole` | string |  |
| `deletedAt` | date |  |
| `email` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `isBlocked` | boolean |  |
| `lastname` | string |  |
| `rate` | number |  |
| `rateStatus` | number |  |
| `rateType` | string |  |
| `screenshots` | string |  |
| `status` | string |  |
| `teamName` | string |  |
| `timezone` | string |  |
| `updatedAt` | date |  |
| `weeklyHoursLimit` | number |  |

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `GET /members` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

