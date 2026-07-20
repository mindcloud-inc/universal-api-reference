# Agile CRM: Create Task

Creates a new task in Agile CRM.

```
POST https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agile CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "Need to contact vendor",
  "type": "CALL",
  "priorityType": "HIGH",
  "due": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "Need to contact vendor",
    "type": "CALL",
    "priorityType": "HIGH",
    "due": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Example: `Need to contact vendor`. |
| `type` | list<string> | yes | One of: `CALL`, `EMAIL`, `FOLLOW_UP`, `MEETING`, `MILESTONE`, `OTHER`, `SEND`, `TWEET`. |
| `priorityType` | list<string> | yes | One of: `HIGH`, `LOW`, `NORMAL`. |
| `due` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "due": 1,
      "entityType": "string",
      "id": 1,
      "isComplete": true,
      "priorityType": "string",
      "progress": 1,
      "status": "string",
      "subject": "string",
      "taskCompletedTime": "2026-05-07T12:00:00.000Z",
      "taskOwner": {
        "calendarUrl": "https://example.com",
        "calendarURL": "https://example.com",
        "domain": "string",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "phone": "string",
        "pic": "string",
        "scheduleId": "string"
      },
      "taskStartTime": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date |  |
| `due` | number |  |
| `entityType` | string |  |
| `id` | number |  |
| `isComplete` | boolean |  |
| `priorityType` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `taskCompletedTime` | date |  |
| `taskOwner.calendarUrl` | string |  |
| `taskOwner.calendarURL` | string |  |
| `taskOwner.domain` | string |  |
| `taskOwner.email` | string |  |
| `taskOwner.id` | number |  |
| `taskOwner.name` | string |  |
| `taskOwner.phone` | string |  |
| `taskOwner.pic` | string |  |
| `taskOwner.scheduleId` | string |  |
| `taskStartTime` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Agile CRM API, this operation is `POST /tasks` (base URL `https://mindcloud.agilecrm.com/dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

