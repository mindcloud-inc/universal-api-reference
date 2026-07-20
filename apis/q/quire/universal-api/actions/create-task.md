# Quire: Create Task

Creates a new task in Quire.

```
POST https://connect.mindcloud.co/v1/universal/quire/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quire/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quire/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The project ID or shortcut, for example App_Account. |
| `name` | string | yes | The title of the new task. |
| `description` | string | no | Optional task description in Markdown. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedBy": {},
      "assignees": [
        {}
      ],
      "assignors": [
        {}
      ],
      "attachments": [
        {}
      ],
      "childCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "description": "string",
      "descriptionHtml": "string",
      "descriptionText": "string",
      "editedBy": {},
      "favorites": [
        {}
      ],
      "followers": [
        {}
      ],
      "id": 1,
      "mutes": [
        {}
      ],
      "name": "Ava Chen",
      "nameHtml": "Ava Chen",
      "nameText": "Ava Chen",
      "oid": "string",
      "partnerBy": {},
      "priority": {},
      "status": {},
      "tags": [
        {}
      ],
      "toggledBy": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedBy` | object |  |
| `assignees` | array<object> |  |
| `assignors` | array<object> |  |
| `attachments` | array<object> |  |
| `childCount` | number |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `description` | string |  |
| `descriptionHtml` | string |  |
| `descriptionText` | string |  |
| `editedBy` | object |  |
| `favorites` | array<object> |  |
| `followers` | array<object> |  |
| `id` | number |  |
| `mutes` | array<object> |  |
| `name` | string |  |
| `nameHtml` | string |  |
| `nameText` | string |  |
| `oid` | string |  |
| `partnerBy` | object |  |
| `priority` | object |  |
| `status` | object |  |
| `tags` | array<object> |  |
| `toggledBy` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Quire API, this operation is `POST task/id/:projectId` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

