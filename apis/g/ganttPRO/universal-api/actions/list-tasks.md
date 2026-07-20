# GanttPRO: List Tasks

Retrieves tasks from a specific GanttPRO project.

```
GET https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-tasks?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-tasks?${params}`, {
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
| `projectId` | number | yes | Required project identifier. GanttPRO accepts this as an array-style query parameter. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `color` | string |  |
| `comments` | array<object> |  |
| `createdAt` | date |  |
| `customFields` | array<object> |  |
| `deadline` | date |  |
| `description` | string |  |
| `duration` | number |  |
| `endDate` | date |  |
| `estimation` | number |  |
| `id` | number |  |
| `links` | array<object> |  |
| `name` | string |  |
| `ownerId` | number |  |
| `parent` | number |  |
| `priority` | number |  |
| `progress` | number |  |
| `projectId` | number |  |
| `resources` | array<object> |  |
| `sortorder` | number |  |
| `startDate` | date |  |
| `status` | number |  |
| `timeLogs` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native GanttPRO API, this operation is `GET /tasks` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

