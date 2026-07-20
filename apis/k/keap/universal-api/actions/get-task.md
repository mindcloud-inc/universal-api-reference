# Keap: Get Task



```
GET https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-task?connectionId=$CONNECTION_ID&task_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-task?${params}`, {
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
| `task_id` | string | yes | The unique identifier of the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": "string",
      "completed": true,
      "contactId": "string",
      "createdByUserId": "string",
      "createTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modificationTime": "2026-05-07T12:00:00.000Z",
      "priority": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | string |  |
| `completed` | boolean |  |
| `contactId` | string |  |
| `createdByUserId` | string |  |
| `createTime` | date |  |
| `id` | string |  |
| `modificationTime` | date |  |
| `priority` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Keap API, this operation is `GET /tasks/:task_id` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

