# Chatwork: List My Tasks



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-my-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-my-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-my-tasks?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedByAccountId` | number | no | Account ID of the user who assigned the task. Example: `12345`. |
| `status` | list<string> | no | Completion status of the task. One of: `done`, `open`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedByAccount": {
        "accountId": 1,
        "avatarImageUrl": "https://example.com",
        "name": "Ava Chen"
      },
      "body": "string",
      "limitTime": 1,
      "limitType": "string",
      "messageId": "string",
      "room": {
        "iconPath": "https://example.com",
        "name": "Ava Chen",
        "roomId": 1
      },
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
| `assignedByAccount.accountId` | number |  |
| `assignedByAccount.avatarImageUrl` | string |  |
| `assignedByAccount.name` | string |  |
| `body` | string |  |
| `limitTime` | number |  |
| `limitType` | string |  |
| `messageId` | string |  |
| `room.iconPath` | string |  |
| `room.name` | string |  |
| `room.roomId` | number |  |
| `status` | string |  |
| `taskId` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /my/tasks` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-my-tasks.md) for the provider-specific parameters and requirements.

