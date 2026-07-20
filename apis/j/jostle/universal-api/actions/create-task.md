# Jostle: Create Task



```
POST https://connect.mindcloud.co/v1/universal/jostle/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jostle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jostle/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title of the task |
| `description` | string | no | Description of the task |
| `dueDate` | string | no | Task due date as an ISO 8601 datetime |
| `assignee.userId` | string | no | Id of the user assigned to the task |
| `assignee.username` | string | no | Username of the user assigned to the task |
| `collaborators.presetId` | string | no | Preset list used to define task collaborators |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedTime": {},
      "createdDate": "string",
      "description": {},
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedTime` | object |  |
| `createdDate` | string |  |
| `description` | object |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Jostle API, this operation is `POST /v2/tasks` (base URL `https://api-prod.jostle.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

