# TaskForce: List Task Messages

Retrieves task conversation messages from TaskForce.

```
GET https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-task-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaskForce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-task-messages?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-task-messages?${params}`, {
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
| `cursor` | string | no | Message cursor for pagination. |
| `limit` | number | no | Maximum number of messages to return. |
| `taskId` | string | yes | Task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {}
      ],
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages` | array<object> | Messages for the task conversation. |
| `nextCursor` | string | Cursor for the next page of messages. |

## Native endpoint

Through the native TaskForce API, this operation is `GET /tasks/:taskId/messages` (base URL `https://www.task-force.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-messages.md) for the provider-specific parameters and requirements.

