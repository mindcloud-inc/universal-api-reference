# Checkvist: Import Tasks

Imports tasks into a checklist in Checkvist.

```
POST https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/import-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/import-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklistId": 1,
  "importContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/import-tasks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklistId": 1,
    "importContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklistId` | number | yes | The checklist ID. |
| `importContent` | string | yes | The checklist content to import. |
| `importContentNote` | string | no | A note to attach to the first created task. |
| `parentId` | number | no | The parent task ID. |
| `parseTasks` | boolean | no | Recognize smart syntax in imported tasks. |
| `position` | number | no | The 1-based position for the first imported task. |
| `replaceExisting` | boolean | no | Replace the existing checklist content. |
| `separateWithEmptyLine` | string | no | Control how imported tasks are split. |
| `status` | number | no | The optional status for the first imported task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeIds": [
        1
      ],
      "backlinkIds": [
        1
      ],
      "checklistId": 1,
      "collapsed": true,
      "commentsCount": 1,
      "content": "string",
      "createdAt": "string",
      "details": {},
      "due": "string",
      "id": 1,
      "linkIds": [
        1
      ],
      "parentId": 1,
      "position": 1,
      "priority": 1,
      "status": 1,
      "tags": {},
      "tagsAsText": "string",
      "tasks": [
        1
      ],
      "updatedAt": "string",
      "updateLine": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeIds` | array<number> |  |
| `backlinkIds` | array<number> |  |
| `checklistId` | number |  |
| `collapsed` | boolean |  |
| `commentsCount` | number |  |
| `content` | string |  |
| `createdAt` | string |  |
| `details` | object |  |
| `due` | string |  |
| `id` | number |  |
| `linkIds` | array<number> |  |
| `parentId` | number |  |
| `position` | number |  |
| `priority` | number |  |
| `status` | number |  |
| `tags` | object |  |
| `tagsAsText` | string |  |
| `tasks` | array<number> |  |
| `updatedAt` | string |  |
| `updateLine` | string |  |

## Native endpoint

Through the native Checkvist API, this operation is `POST /checklists/:checklistId/import.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-tasks.md) for the provider-specific parameters and requirements.

