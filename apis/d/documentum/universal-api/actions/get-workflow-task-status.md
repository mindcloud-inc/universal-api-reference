# Documentum: Get Workflow Task Status



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-workflow-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-workflow-task-status?connectionId=$CONNECTION_ID&repositoryName=d2repo&processName=Review%20Process&processId=4d00000180001234&taskName=Review%20Task&taskId=4a00000180005678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "processName": "Review Process",
  "processId": "4d00000180001234",
  "taskName": "Review Task",
  "taskId": "4a00000180005678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-workflow-task-status?${params}`, {
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
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `processName` | string | yes | Name of the dm_workflow process. Example: `Review Process`. |
| `processId` | string | yes | r_object_id of the dm_workflow process. Example: `4d00000180001234`. |
| `taskName` | string | yes | Name of the workflow activity. Example: `Review Task`. |
| `taskId` | string | yes | r_object_id of the dmi_queue_item task. Example: `4a00000180005678`. |

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
      "status": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
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
| `status` | string | Workflow task status. |
| `title` | string | Task title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/processes/{processName}/{processId}/{taskName}/{taskId}/status` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-task-status.md) for the provider-specific parameters and requirements.

