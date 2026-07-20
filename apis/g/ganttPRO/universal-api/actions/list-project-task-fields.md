# GanttPRO: List Project Task Fields

Retrieves task fields for a specific GanttPRO project.

```
GET https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-project-task-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-project-task-fields?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-project-task-fields?${params}`, {
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
| `projectId` | number | yes | Project identifier used to return task field definitions for one project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isCustom": true,
      "key": "string",
      "name": "Ava Chen",
      "options": [
        {}
      ],
      "type": "string",
      "writable": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isCustom` | boolean |  |
| `key` | string |  |
| `name` | string |  |
| `options` | array<object> |  |
| `type` | string |  |
| `writable` | number |  |

## Native endpoint

Through the native GanttPRO API, this operation is `GET /projects/taskFields` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-task-fields.md) for the provider-specific parameters and requirements.

