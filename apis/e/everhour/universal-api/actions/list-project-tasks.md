# Everhour: List Project Tasks

Retrieves tasks for a project from Everhour.

```
GET https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-project-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-project-tasks?${params}`, {
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
| `limit` | number | no | Maximum number of records to return. |
| `page` | number | no | Page number to return. |
| `projectId` | string | yes | Everhour project ID. |
| `query` | string | no | Filter tasks by name or search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
      "completed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "id": "string",
      "labels": [
        {}
      ],
      "name": "Ava Chen",
      "position": 1,
      "projects": [
        "string"
      ],
      "section": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> |  |
| `completed` | boolean |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `id` | string |  |
| `labels` | array<object> |  |
| `name` | string |  |
| `position` | number |  |
| `projects` | array<string> |  |
| `section` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Everhour API, this operation is `GET /projects/:projectId/tasks` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-tasks.md) for the provider-specific parameters and requirements.

