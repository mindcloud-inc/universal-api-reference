# Shortcut: Update Story



```
PUT https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/update-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/update-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storyPublicId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/update-story', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storyPublicId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storyPublicId` | number | yes |  |
| `name` | string | no |  |
| `description` | string | no |  |
| `storyType` | string | no |  |
| `epicId` | number | no |  |
| `requestedById` | string | no |  |
| `iterationId` | number | no |  |
| `groupId` | string | no |  |
| `workflowStateId` | number | no |  |
| `parentStoryId` | number | no |  |
| `estimate` | number | no |  |
| `projectId` | number | no |  |
| `deadline` | string | no |  |
| `archived` | boolean | no |  |
| `beforeId` | number | no |  |
| `afterId` | number | no |  |
| `completedAtOverride` | string | no |  |
| `startedAtOverride` | string | no |  |

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

Through the native Shortcut API, this operation is `PUT /stories/:storyPublicId` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-story.md) for the provider-specific parameters and requirements.

