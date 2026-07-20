# Habitica: Delete Task

Deletes an existing task from Habitica.

```
DELETE https://connect.mindcloud.co/v1/universal/habitica/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/delete-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/habitica/latest/actions/delete-task?${params}`, {
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
| `taskId` | string | yes | The Habitica task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appVersion": "string",
      "data": [
        {}
      ],
      "notifications": [
        {}
      ],
      "success": true,
      "userV": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appVersion` | string |  |
| `data` | array<object> |  |
| `notifications` | array<object> |  |
| `success` | boolean |  |
| `userV` | number |  |

## Native endpoint

Through the native Habitica API, this operation is `DELETE /tasks/:taskId` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

