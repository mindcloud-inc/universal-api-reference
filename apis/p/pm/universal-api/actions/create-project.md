# 5pm: Create Project

Creates a new project in 5pm.

```
POST https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pm/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project.name` | string | yes | Name of the project to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "groupId": 1,
      "id": "string",
      "name": "Ava Chen",
      "ownerId": 1,
      "priority": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Project description. |
| `groupId` | number | Project group ID. |
| `id` | string | Project identifier. |
| `name` | string | Project name. |
| `ownerId` | number | Project owner user ID. |
| `priority` | number | Project priority ID. |
| `status` | number | Project status ID. |

## Native endpoint

Through the native 5pm API, this operation is `POST /service/post/projects/add` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

