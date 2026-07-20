# ClickUp: Create List



```
POST https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "folderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "folderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignee` | number | no |  |
| `name` | string | yes |  |
| `content` | string | no |  |
| `dueDate` | date | no |  |
| `dueDateTime` | boolean | no |  |
| `folderId` | string | yes |  |
| `markdownContent` | string | no |  |
| `priority` | list | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {
        "color": "string",
        "id": 1,
        "initials": "string",
        "profilePicture": "string",
        "username": "Ava Chen"
      },
      "content": "string",
      "dueDate": "string",
      "dueDateTime": true,
      "folder": {
        "access": true,
        "hidden": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "inboundAddress": "string",
      "name": "Ava Chen",
      "orderindex": 1,
      "priority": {
        "color": "string",
        "priority": "string"
      },
      "space": {
        "access": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "startDate": "string",
      "startDateTime": "string",
      "status": {
        "color": "string",
        "hideLabel": true,
        "status": "string"
      },
      "statuses": [
        {
          "color": "string",
          "id": "string",
          "orderindex": 1,
          "status": "string",
          "type": "string"
        }
      ],
      "taskCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `assignee.color` | string |  |
| `assignee.id` | number |  |
| `assignee.initials` | string |  |
| `assignee.profilePicture` | string |  |
| `assignee.username` | string |  |
| `content` | string |  |
| `dueDate` | string |  |
| `dueDateTime` | boolean |  |
| `folder` | object |  |
| `folder.access` | boolean |  |
| `folder.hidden` | boolean |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `id` | string |  |
| `inboundAddress` | string |  |
| `name` | string |  |
| `orderindex` | number |  |
| `priority` | object |  |
| `priority.color` | string |  |
| `priority.priority` | string |  |
| `space` | object |  |
| `space.access` | boolean |  |
| `space.id` | string |  |
| `space.name` | string |  |
| `startDate` | string |  |
| `startDateTime` | string |  |
| `status` | object |  |
| `status.color` | string |  |
| `status.hideLabel` | boolean |  |
| `status.status` | string |  |
| `statuses` | array |  |
| `statuses[]` | object |  |
| `statuses[].color` | string |  |
| `statuses[].id` | string |  |
| `statuses[].orderindex` | number |  |
| `statuses[].status` | string |  |
| `statuses[].type` | string |  |
| `taskCount` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `POST folder/:folder_id/list` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

