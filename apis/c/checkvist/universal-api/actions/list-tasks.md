# Checkvist: List Tasks

Retrieves tasks from Checkvist.

```
GET https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/list-tasks?connectionId=$CONNECTION_ID&checklistId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checklistId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/list-tasks?${params}`, {
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
| `checklistId` | number | yes | The checklist ID. |
| `order` | string | no | Sort tasks, for example updated_at:asc or id:desc. |
| `withNotes` | boolean | no | Include task notes in the response. |

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
      "updateLine": "string",
      "uploads": [
        {}
      ]
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
| `uploads` | array<object> |  |

## Native endpoint

Through the native Checkvist API, this operation is `GET /checklists/:checklistId/tasks.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

