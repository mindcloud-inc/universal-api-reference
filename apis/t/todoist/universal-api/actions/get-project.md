# Todoist: Get Project

Retrieves project details from Todoist.

```
GET https://connect.mindcloud.co/v1/universal/todoist/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/todoist/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | Project identifier. |

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

Through the native Todoist API, this operation is `GET /api/v1/projects/:project_id` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

