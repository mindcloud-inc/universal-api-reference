# ClickUp: Create List View

Creates a new view for a ClickUp List.

```
POST https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-list-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-list-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "name": "Ava Chen",
  "columns.fields[]": [
    "string"
  ],
  "filters.operator": "string",
  "grouping.field": "string",
  "sorting.fields[]": [
    "string"
  ],
  "filters.fields[]": [
    {}
  ],
  "grouping.dir": 1,
  "type": "string",
  "filters.showClosed": true,
  "grouping": {},
  "divide": {},
  "sorting": {},
  "filters": {},
  "columns": {},
  "teamSidebar": {},
  "settings": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-list-view', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "name": "Ava Chen",
    "columns.fields[]": ["string"],
    "filters.operator": "string",
    "grouping.field": "string",
    "sorting.fields[]": ["string"],
    "filters.fields[]": [{}],
    "grouping.dir": 1,
    "type": "string",
    "filters.showClosed": true,
    "grouping": {},
    "divide": {},
    "sorting": {},
    "filters": {},
    "columns": {},
    "teamSidebar": {},
    "settings": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes |  |
| `name` | string | yes |  |
| `columns.fields[]` | array | yes |  |
| `divide.collapsed[]` | array<string> | no |  |
| `filters.operator` | string | yes |  |
| `grouping.field` | string | yes |  |
| `sorting.fields[]` | array | yes |  |
| `filters.fields[]` | array<object> | yes |  |
| `grouping.dir` | number | yes |  |
| `filters.search` | string | no |  |
| `grouping.collapsed[]` | array<string> | no |  |
| `type` | string | yes |  |
| `filters.showClosed` | boolean | yes |  |
| `grouping` | object | yes |  |
| `grouping.ignore` | boolean | no |  |
| `divide` | object | yes |  |
| `sorting` | object | yes |  |
| `filters` | object | yes |  |
| `columns` | object | yes |  |
| `teamSidebar` | object | yes |  |
| `settings` | object | yes |  |

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

Through the native ClickUp API, this operation is `POST list/:list_id/view` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list-view.md) for the provider-specific parameters and requirements.

