# Jostle: Create Tasks for Many Assignees



```
POST https://connect.mindcloud.co/v1/universal/jostle/latest/actions/create-tasks-for-many-assignees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jostle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/create-tasks-for-many-assignees" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jostle/latest/actions/create-tasks-for-many-assignees', {
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
| `assignees.users[].userId` | string | no | Id of a user who should receive a duplicated task |
| `assignees.users[].username` | string | no | Username of a user who should receive a duplicated task |
| `assignees.presetId` | string | no | Preset list used to select assignees |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": "string",
      "id": "string",
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | string |  |
| `id` | string |  |
| `success` | string |  |

## Native endpoint

Through the native Jostle API, this operation is `POST /v2/tasks/duplicate` (base URL `https://api-prod.jostle.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tasks-for-many-assignees.md) for the provider-specific parameters and requirements.

