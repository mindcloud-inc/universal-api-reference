# Chatwork: Get Chat Message



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-message?connectionId=$CONNECTION_ID&roomId=12345&messageId=101" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "12345",
  "messageId": "101"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-message?${params}`, {
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
| `roomId` | number | yes | Room ID Example: `12345`. |
| `messageId` | string | yes | Message ID Example: `101`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "accountId": 1,
        "avatarImageUrl": "https://example.com",
        "name": "Ava Chen"
      },
      "body": "string",
      "messageId": "string",
      "sendTime": 1,
      "updateTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.accountId` | number |  |
| `account.avatarImageUrl` | string |  |
| `account.name` | string |  |
| `body` | string |  |
| `messageId` | string |  |
| `sendTime` | number |  |
| `updateTime` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /rooms/:room_id/messages/:message_id` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-message.md) for the provider-specific parameters and requirements.

