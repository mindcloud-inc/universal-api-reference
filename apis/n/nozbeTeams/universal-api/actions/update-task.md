# Nozbe Teams: Update Task

Updates an existing task in Nozbe Teams.

```
PUT https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The task to update. |
| `name` | string | no | The updated task name. |

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

Through the native Nozbe Teams API, this operation is `PUT /tasks/:id` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

