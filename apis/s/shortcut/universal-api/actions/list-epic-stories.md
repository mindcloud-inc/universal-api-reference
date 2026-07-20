# Shortcut: List Epic Stories



```
GET https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-epic-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-epic-stories?connectionId=$CONNECTION_ID&epicPublicId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "epicPublicId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-epic-stories?${params}`, {
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
| `epicPublicId` | number | yes | The public ID of the epic. |
| `includesDescription` | boolean | no | Whether to include story descriptions in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "completed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "entityType": "string",
      "epicId": 1,
      "estimate": 1,
      "groupId": "string",
      "id": 1,
      "iterationId": 1,
      "movedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "projectId": 1,
      "requestedById": "string",
      "started": true,
      "storyType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workflowStateId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `completed` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `entityType` | string |  |
| `epicId` | number |  |
| `estimate` | number |  |
| `groupId` | string |  |
| `id` | number |  |
| `iterationId` | number |  |
| `movedAt` | date |  |
| `name` | string |  |
| `projectId` | number |  |
| `requestedById` | string |  |
| `started` | boolean |  |
| `storyType` | string |  |
| `updatedAt` | date |  |
| `workflowStateId` | number |  |

## Native endpoint

Through the native Shortcut API, this operation is `GET /epics/:epicPublicId/stories` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-epic-stories.md) for the provider-specific parameters and requirements.

