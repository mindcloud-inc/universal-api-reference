# Microsoft Teams: Soft Delete Chat Message



```
DELETE https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/soft-delete-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/soft-delete-chat-message?connectionId=$CONNECTION_ID&userId=string&chatId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string",
  "chatId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/soft-delete-chat-message?${params}`, {
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
| `userId` | string | yes |  |
| `chatId` | string | yes |  |
| `messageId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Teams API returns.

## Native endpoint

Through the native Microsoft Teams API, this operation is `POST /v1.0/users/:userId/chats/:chatId/messages/:messageId/softDelete` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/soft-delete-chat-message.md) for the provider-specific parameters and requirements.

