# Chatwork: Get Chat File



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-file?connectionId=$CONNECTION_ID&roomId=123456789&fileId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "123456789",
  "fileId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-chat-file?${params}`, {
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
| `fileId` | number | yes | File ID. Example: `123456789`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createDownloadUrl` | number | no | Set to 1 to include a temporary download URL valid for 30 seconds. Default: `0`. Example: `1`. |

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
      "downloadUrl": "https://example.com",
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
| `downloadUrl` | string |  |
| `fileId` | number |  |
| `filename` | string |  |
| `filesize` | number |  |
| `messageId` | string |  |
| `uploadTime` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /rooms/:room_id/files/:file_id` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-file.md) for the provider-specific parameters and requirements.

