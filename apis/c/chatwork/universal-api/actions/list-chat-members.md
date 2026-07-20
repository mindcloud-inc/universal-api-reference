# Chatwork: List Chat Members



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chat-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chat-members?connectionId=$CONNECTION_ID&roomId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/list-chat-members?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "avatarImageUrl": "https://example.com",
      "chatworkId": "string",
      "department": "string",
      "name": "Ava Chen",
      "organizationId": 1,
      "organizationName": "Ava Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `avatarImageUrl` | string |  |
| `chatworkId` | string |  |
| `department` | string |  |
| `name` | string |  |
| `organizationId` | number |  |
| `organizationName` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /rooms/:room_id/members` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-members.md) for the provider-specific parameters and requirements.

