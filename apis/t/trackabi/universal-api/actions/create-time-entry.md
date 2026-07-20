# Trackabi: Create Time Entry

Creates a new time entry in Trackabi.

```
POST https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memberId` | number | no | Member ID. Do not use together with email. |
| `email` | string | no | Member email. Do not use together with member ID. |
| `clientId` | number | no | Client ID. Do not use together with client name. |
| `clientName` | string | no | Client name. Do not use together with client ID. |
| `projectId` | number | no | Project ID. Do not use together with project name. |
| `projectName` | string | no | Project name. Do not use together with project ID. |
| `taskId` | number | no | Task ID. Do not use together with task name. |
| `taskName` | string | no | Task name. Do not use together with task ID. |
| `dateLogged` | date | no | Date logged in YYYY-MM-DD format. |
| `description` | string | no | Description of work. |
| `loggedTime` | string | no | Logged time in HH:MM:SS format. |
| `billable` | string | no | Billable time in HH:MM:SS format. |
| `startTime` | string | no | Start time in HH:MM:SS format. |
| `endTime` | string | no | End time in HH:MM:SS format. |
| `timeType` | string | no | Name of time type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": "string",
      "client": {
        "id": 1,
        "logo": "string",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      },
      "dateLogged": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endTime": "string",
      "id": 1,
      "loggedTime": "string",
      "member": {
        "avatar": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen"
      },
      "project": {
        "id": 1,
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      },
      "startTime": "string",
      "task": {
        "id": 1,
        "name": "Ava Chen",
        "parentTaskId": 1
      },
      "timerStartedAt": "string",
      "timeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | string |  |
| `client.id` | number |  |
| `client.logo` | string |  |
| `client.name` | string |  |
| `client.shortName` | string |  |
| `dateLogged` | date |  |
| `description` | string |  |
| `endTime` | string |  |
| `id` | number |  |
| `loggedTime` | string |  |
| `member.avatar` | string |  |
| `member.email` | string |  |
| `member.firstName` | string |  |
| `member.id` | number |  |
| `member.lastName` | string |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `project.shortName` | string |  |
| `startTime` | string |  |
| `task.id` | number |  |
| `task.name` | string |  |
| `task.parentTaskId` | number |  |
| `timerStartedAt` | string |  |
| `timeType` | string |  |

## Native endpoint

Through the native Trackabi API, this operation is `POST /api/v1/time-entries` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

