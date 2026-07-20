# Communi App: List User Conversations



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-user-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-user-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-user-conversations?${params}`, {
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
| `user` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "conversation": "string",
      "id": "string",
      "isMarkedUnseen": true,
      "lastMessageReceivedSerialId": 1,
      "lastMessageSeenSerialId": 1,
      "mute": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_loadStatus` | number |  |
| `_rls` | number |  |
| `conversation` | string |  |
| `id` | string |  |
| `isMarkedUnseen` | boolean |  |
| `lastMessageReceivedSerialId` | number |  |
| `lastMessageSeenSerialId` | number |  |
| `mute` | number |  |
| `user` | number |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/userConversation` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-conversations.md) for the provider-specific parameters and requirements.

