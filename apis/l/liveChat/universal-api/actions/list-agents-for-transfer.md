# LiveChat: List Agents For Transfer

Retrieves agents available for chat transfer in LiveChat.

```
GET https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-agents-for-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-agents-for-transfer?connectionId=$CONNECTION_ID&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/list-agents-for-transfer?${params}`, {
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
| `chatId` | string | yes | The chat ID to inspect for transfer targets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "totalActiveChats": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Agent identifier. |
| `totalActiveChats` | number | Number of active customer chats assigned to the agent. |

## Native endpoint

Through the native LiveChat API, this operation is `POST /list_agents_for_transfer` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents-for-transfer.md) for the provider-specific parameters and requirements.

