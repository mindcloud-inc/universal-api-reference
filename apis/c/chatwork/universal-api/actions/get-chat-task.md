# Chatwork: Get Chat Task



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-task?connectionId=$CONNECTION_ID&roomId=123456789&taskId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "123456789",
  "taskId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-task?${params}`, {
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
| `roomId` | number | yes | Room ID. Example: `123456789`. |
| `taskId` | number | yes | Task ID. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "assignedByAccount": {},
      "body": "string",
      "limitTime": 1,
      "limitType": "string",
      "messageId": "string",
      "status": "string",
      "taskId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `assignedByAccount` | object |  |
| `body` | string |  |
| `limitTime` | number |  |
| `limitType` | string |  |
| `messageId` | string |  |
| `status` | string |  |
| `taskId` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /rooms/:room_id/tasks/:task_id` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-task.md) for the provider-specific parameters and requirements.

