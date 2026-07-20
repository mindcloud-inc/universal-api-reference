# Chatwork: Get My Status



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-status?${params}`, {
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
      "mentionNum": 1,
      "mentionRoomNum": 1,
      "mytaskNum": 1,
      "mytaskRoomNum": 1,
      "unreadNum": 1,
      "unreadRoomNum": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mentionNum` | number |  |
| `mentionRoomNum` | number |  |
| `mytaskNum` | number |  |
| `mytaskRoomNum` | number |  |
| `unreadNum` | number |  |
| `unreadRoomNum` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /my/status` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-status.md) for the provider-specific parameters and requirements.

