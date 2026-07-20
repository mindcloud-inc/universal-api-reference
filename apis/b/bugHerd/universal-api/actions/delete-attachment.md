# BugHerd: Delete Attachment

Deletes an attachment from a BugHerd task.

```
DELETE https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/delete-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/delete-attachment?connectionId=$CONNECTION_ID&projectId=1&taskId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "taskId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/delete-attachment?${params}`, {
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
| `projectId` | number | yes | The BugHerd project ID. |
| `taskId` | number | yes | The BugHerd task ID. |
| `id` | number | yes | The BugHerd attachment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native BugHerd API, this operation is `DELETE projects/:project_id/tasks/:task_id/attachments/:id.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-attachment.md) for the provider-specific parameters and requirements.

