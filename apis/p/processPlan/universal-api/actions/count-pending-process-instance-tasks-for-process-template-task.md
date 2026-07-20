# Process Plan: Count Pending Process Instance Tasks for Process Template Task



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/count-pending-process-instance-tasks-for-process-template-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/count-pending-process-instance-tasks-for-process-template-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/count-pending-process-instance-tasks-for-process-template-task?${params}`, {
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
| `processTemplateTaskId` | string | no | Process template task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_task/:processTemplateTaskId/process_instance_task/list/pending/count` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-pending-process-instance-tasks-for-process-template-task.md) for the provider-specific parameters and requirements.

