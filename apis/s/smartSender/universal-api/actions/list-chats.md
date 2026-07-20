# Smart Sender: List Chats

Retrieves project chats from Smart Sender.

```
GET https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-chats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-chats?${params}`, {
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
      "canReply": true,
      "id": 1,
      "image": "string",
      "isClosed": true,
      "lastMessage": {},
      "phone": "string",
      "state": {},
      "timeAnswer": "2026-05-07T12:00:00.000Z",
      "timeClose": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "type": "string",
      "unreadMessages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canReply` | boolean |  |
| `id` | number |  |
| `image` | string |  |
| `isClosed` | boolean |  |
| `lastMessage` | object |  |
| `phone` | string |  |
| `state` | object |  |
| `timeAnswer` | date |  |
| `timeClose` | date |  |
| `title` | string |  |
| `type` | string |  |
| `unreadMessages` | number |  |

## Native endpoint

Through the native Smart Sender API, this operation is `GET /v1/chats` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

