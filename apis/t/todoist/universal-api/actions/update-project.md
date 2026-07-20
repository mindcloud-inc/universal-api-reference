# Todoist: Update Project

Updates an existing project in Todoist.

```
PUT https://connect.mindcloud.co/v1/universal/todoist/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/todoist/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project identifier. |
| `name` | string | no | Project name. |
| `description` | string | no | Project description. |
| `color` | string | no | Project color. |
| `isFavorite` | boolean | no | Mark as favorite. |
| `viewStyle` | string | no | Project view style (list, board, or calendar). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canAssignTasks": true,
      "childOrder": 1,
      "color": "string",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "inboxProject": true,
      "isFavorite": true,
      "isShared": true,
      "name": "Ava Chen",
      "parentId": "string",
      "role": "string",
      "updatedAt": "string",
      "viewStyle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canAssignTasks` | boolean | Whether tasks can be assigned |
| `childOrder` | number | Display order |
| `color` | string | Project color |
| `createdAt` | string | Creation timestamp |
| `description` | string | Project description |
| `id` | string | Project ID |
| `inboxProject` | boolean | Whether this is inbox project |
| `isFavorite` | boolean | Whether project is favorite |
| `isShared` | boolean | Whether project is shared |
| `name` | string | Project name |
| `parentId` | string | Parent project ID |
| `role` | string | User role for project |
| `updatedAt` | string | Update timestamp |
| `viewStyle` | string | Project view style |

## Native endpoint

Through the native Todoist API, this operation is `POST /api/v1/projects/:project_id` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

