# GanttPRO: Create Task

Creates a new task in GanttPRO.

```
POST https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Project identifier for the new task. |
| `name` | string | yes | Task name. |
| `parent` | number | no | Optional parent task identifier. |
| `startDate` | date | no | Task start date. |
| `endDate` | date | no | Task end date. |
| `description` | string | no | Task description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "attachments": [
          {}
        ],
        "color": "string",
        "comments": [
          {}
        ],
        "createdAt": "2026-05-07T12:00:00.000Z",
        "customFields": [
          {}
        ],
        "deadline": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "duration": 1,
        "endDate": "2026-05-07T12:00:00.000Z",
        "estimation": 1,
        "id": 1,
        "links": [
          {}
        ],
        "name": "Ava Chen",
        "ownerId": 1,
        "parent": 1,
        "priority": 1,
        "progress": 1,
        "projectId": 1,
        "resources": [
          {}
        ],
        "sortorder": 1,
        "startDate": "2026-05-07T12:00:00.000Z",
        "status": 1,
        "timeLogs": [
          {}
        ],
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item.attachments` | array<object> |  |
| `item.color` | string |  |
| `item.comments` | array<object> |  |
| `item.createdAt` | date |  |
| `item.customFields` | array<object> |  |
| `item.deadline` | date |  |
| `item.description` | string |  |
| `item.duration` | number |  |
| `item.endDate` | date |  |
| `item.estimation` | number |  |
| `item.id` | number |  |
| `item.links` | array<object> |  |
| `item.name` | string |  |
| `item.ownerId` | number |  |
| `item.parent` | number |  |
| `item.priority` | number |  |
| `item.progress` | number |  |
| `item.projectId` | number |  |
| `item.resources` | array<object> |  |
| `item.sortorder` | number |  |
| `item.startDate` | date |  |
| `item.status` | number |  |
| `item.timeLogs` | array<object> |  |
| `item.type` | string |  |

## Native endpoint

Through the native GanttPRO API, this operation is `POST /tasks` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

