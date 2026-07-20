# PiAPI/Kling: List User Task History



```
GET https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/list-user-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/list-user-task-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/list-user-task-history?${params}`, {
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
| `page` | number | no | Page number. PiAPI starts paging at 1. |
| `pageSize` | number | no | Number of history records to return. PiAPI defaults to 10 and allows up to 100. |
| `model` | string | no | Filter history to one PiAPI model. Use kling for Kling tasks. Default: `kling`. |
| `startTime` | number | no | Unix timestamp in seconds. Return tasks created at or after this time. |
| `endTime` | number | no | Unix timestamp in seconds. Return tasks created at or before this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "action": "string",
      "apiKeyId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "detail": {},
      "fixed": true,
      "id": 1,
      "serviceMode": "string",
      "status": "string",
      "taskId": "string",
      "taskModel": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usage": 1,
      "usageType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Owning PiAPI account identifier. |
| `action` | string | Task action type. |
| `apiKeyId` | number | PiAPI API key identifier that created the task. |
| `createdAt` | date | History record creation timestamp. |
| `deletedAt` | date | History record deletion timestamp when present. |
| `detail` | object | Failure or detail payload from PiAPI. |
| `fixed` | boolean | Whether the record was marked fixed by PiAPI. |
| `id` | number | PiAPI history row identifier. |
| `serviceMode` | string | Service mode used for the task. |
| `status` | string | Recorded task status. |
| `taskId` | string | Referenced PiAPI task identifier. |
| `taskModel` | string | Provider model name. |
| `updatedAt` | date | History record update timestamp. |
| `usage` | number | Consumed usage amount. |
| `usageType` | string | Billing usage unit. |

## Native endpoint

Through the native PiAPI/Kling API, this operation is `GET /api/open/tasks/histories` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-task-history.md) for the provider-specific parameters and requirements.

