# Trackabi: Get Time Entry

Retrieves a time entry from Trackabi.

```
GET https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-time-entry?connectionId=$CONNECTION_ID&timeEntryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeEntryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-time-entry?${params}`, {
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
| `timeEntryId` | number | yes | The unique ID of the time entry. |

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

Through the native Trackabi API, this operation is `GET /api/v1/time-entry/:timeEntryId` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry.md) for the provider-specific parameters and requirements.

