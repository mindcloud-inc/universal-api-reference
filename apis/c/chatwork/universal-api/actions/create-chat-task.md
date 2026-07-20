# Chatwork: Create Chat Task



```
POST https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/create-chat-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/create-chat-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "123456789",
  "body": "Buy milk",
  "toIds": "1,3,6"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/create-chat-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "123456789",
    "body": "Buy milk",
    "toIds": "1,3,6"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Room ID. Example: `123456789`. |
| `body` | string | yes | Task content. Example: `Buy milk`. |
| `toIds` | string | yes | Comma-separated account IDs assigned to the task. Accepts multiple values in one string, delimited by `,`. Example: `1,3,6`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Unix timestamp in seconds for the task deadline. Example: `1385996399`. |
| `limitType` | list<string> | no | Deadline interpretation. One of: `date`, `none`, `time`. Default: `time`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskIds` | array<number> |  |

## Native endpoint

Through the native Chatwork API, this operation is `POST /rooms/:room_id/tasks` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-task.md) for the provider-specific parameters and requirements.

