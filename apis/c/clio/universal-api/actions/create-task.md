# Clio Manage: Create Task

Creates a new task in Clio Manage.

```
POST https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.name": "Ava Chen",
  "data.description": "string",
  "data.assignee.id": 1,
  "data.assignee.type": "Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.name": "Ava Chen",
    "data.description": "string",
    "data.assignee.id": 1,
    "data.assignee.type": "Contact"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.name` | string | yes |  |
| `data.description` | string | yes |  |
| `data.assignee.id` | number | yes |  |
| `data.assignee.type` | list | yes | One of: `Contact`, `User`. |
| `data.matter.id` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Clio Manage API, this operation is `POST /tasks.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

