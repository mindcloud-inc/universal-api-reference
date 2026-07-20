# DoneDone: Delete Task

Deletes an existing task from DoneDone.

```
DELETE https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/delete-task?connectionId=$CONNECTION_ID&accountId=1&projectId=1&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "projectId": "1",
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/delete-task?${params}`, {
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
| `accountId` | number | yes | DoneDone account ID. |
| `projectId` | number | yes | DoneDone internal project ID. |
| `taskId` | number | yes | DoneDone task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider confirmation message. |

## Native endpoint

Through the native DoneDone API, this operation is `DELETE /:account_id/internal-projects/:internal_project_id/tasks/:task_id` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

