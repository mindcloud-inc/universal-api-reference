# Wrike: Delete Task

Deletes an existing task from Wrike.

```
DELETE https://connect.mindcloud.co/v1/universal/wrike/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/delete-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/delete-task?${params}`, {
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
| `taskId` | string | yes | Wrike task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "customStatusId": "string",
      "dates": {},
      "entityTypeId": "string",
      "id": "string",
      "importance": "string",
      "permalink": "https://example.com",
      "priority": "string",
      "scope": "string",
      "status": "string",
      "title": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdDate` | date |  |
| `customStatusId` | string |  |
| `dates` | object |  |
| `entityTypeId` | string |  |
| `id` | string |  |
| `importance` | string |  |
| `permalink` | string |  |
| `priority` | string |  |
| `scope` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Wrike API, this operation is `DELETE /tasks/:taskId` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

