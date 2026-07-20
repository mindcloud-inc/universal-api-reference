# Documentum: Update Workflow Task Status



```
PUT https://connect.mindcloud.co/v1/universal/documentum/latest/actions/update-workflow-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/update-workflow-task-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "repositoryName": "d2repo",
  "processName": "Review Process",
  "processId": "4d00000180001234",
  "taskName": "Review Task",
  "taskId": "4a00000180005678",
  "properties": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentum/latest/actions/update-workflow-task-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "repositoryName": "d2repo",
    "processName": "Review Process",
    "processId": "4d00000180001234",
    "taskName": "Review Task",
    "taskId": "4a00000180005678",
    "properties": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `processName` | string | yes | Name of the dm_workflow process. Example: `Review Process`. |
| `processId` | string | yes | r_object_id of the dm_workflow process. Example: `4d00000180001234`. |
| `taskName` | string | yes | Name of the workflow activity. Example: `Review Task`. |
| `taskId` | string | yes | r_object_id of the dmi_queue_item task. Example: `4a00000180005678`. |
| `properties` | object | yes | JSON task action payload, for example action, comment, next_task_id, user, or signoff fields. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "rel": "https://example.com"
        }
      ],
      "message": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Task identifier. |
| `links[].href` | string | Task link URL. |
| `links[].rel` | string | Task link relation. |
| `message` | string | Status update message. |
| `status` | string | Updated workflow task status. |
| `title` | string | Task title. |

## Native endpoint

Through the native Documentum API, this operation is `POST /repositories/{repositoryName}/processes/{processName}/{processId}/{taskName}/{taskId}/status` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow-task-status.md) for the provider-specific parameters and requirements.

