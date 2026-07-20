# Chatwork: List Chat Files



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chat-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chat-files?connectionId=$CONNECTION_ID&roomId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chat-files?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | no | Account ID of the file uploader. Example: `12345`. |

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
      "fileId": 1,
      "filename": "Ava Chen",
      "filesize": 1,
      "messageId": "string",
      "uploadTime": 1
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
| `fileId` | number |  |
| `filename` | string |  |
| `filesize` | number |  |
| `messageId` | string |  |
| `uploadTime` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /rooms/:room_id/files` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-files.md) for the provider-specific parameters and requirements.

