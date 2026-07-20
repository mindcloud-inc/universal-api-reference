# Nozbe Teams: Create Task

Creates a new task in Nozbe Teams.

```
POST https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The task name. |
| `projectId` | string | yes | The project that will contain the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "createdAt": 1,
      "extra": "string",
      "id": "string",
      "isAbandoned": true,
      "isAllDay": true,
      "isFollowed": true,
      "lastActivityAt": 1,
      "lastModified": 1,
      "missedRepeats": 1,
      "name": "Ava Chen",
      "projectId": "string",
      "projectPosition": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `createdAt` | number |  |
| `extra` | string |  |
| `id` | string |  |
| `isAbandoned` | boolean |  |
| `isAllDay` | boolean |  |
| `isFollowed` | boolean |  |
| `lastActivityAt` | number |  |
| `lastModified` | number |  |
| `missedRepeats` | number |  |
| `name` | string |  |
| `projectId` | string |  |
| `projectPosition` | number |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `POST /tasks` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

