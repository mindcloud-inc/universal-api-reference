# Chatwork: List Chats



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "fileNum": 1,
      "iconPath": "string",
      "lastUpdateTime": 1,
      "mentionNum": 1,
      "messageNum": 1,
      "mytaskNum": 1,
      "name": "Ava Chen",
      "role": "string",
      "roomId": 1,
      "sticky": true,
      "taskNum": 1,
      "type": "string",
      "unreadNum": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileNum` | number |  |
| `iconPath` | string |  |
| `lastUpdateTime` | number |  |
| `mentionNum` | number |  |
| `messageNum` | number |  |
| `mytaskNum` | number |  |
| `name` | string |  |
| `role` | string |  |
| `roomId` | number |  |
| `sticky` | boolean |  |
| `taskNum` | number |  |
| `type` | string |  |
| `unreadNum` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /rooms` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

