# Chatwork: Leave or Delete Chat



```
DELETE https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/leave-or-delete-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/leave-or-delete-chat?connectionId=$CONNECTION_ID&roomId=12345&actionType=delete" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "12345",
  "actionType": "delete"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/leave-or-delete-chat?${params}`, {
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
| `actionType` | list<string> | yes | Whether to leave or delete the room One of: `delete`, `leave`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "roomId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `roomId` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `DELETE /rooms/:room_id` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/leave-or-delete-chat.md) for the provider-specific parameters and requirements.

