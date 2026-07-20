# GanttPRO: Remove Resource From Task

Removes resources from an existing GanttPRO task.

```
DELETE https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/remove-resource-from-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/remove-resource-from-task?connectionId=$CONNECTION_ID&taskId=1&resourceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1",
  "resourceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/remove-resource-from-task?${params}`, {
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
| `taskId` | number | yes | GanttPRO task identifier. |
| `resourceId` | number | yes | Resource identifier or identifiers to remove from the task. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native GanttPRO API, this operation is `DELETE /tasks/:taskId/assignResource` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-resource-from-task.md) for the provider-specific parameters and requirements.

