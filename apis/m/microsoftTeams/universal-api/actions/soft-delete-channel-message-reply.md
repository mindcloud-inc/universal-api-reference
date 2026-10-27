# Microsoft Teams: Soft Delete Channel Message Reply



```
DELETE https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/soft-delete-channel-message-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/soft-delete-channel-message-reply?connectionId=$CONNECTION_ID&teamId=string&channelId=string&messageId=string&replyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "channelId": "string",
  "messageId": "string",
  "replyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/soft-delete-channel-message-reply?${params}`, {
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
| `teamId` | string | yes |  |
| `channelId` | string | yes |  |
| `messageId` | string | yes |  |
| `replyId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Teams API returns.

## Native endpoint

Through the native Microsoft Teams API, this operation is `POST /v1.0/teams/:teamId/channels/:channelId/messages/:messageId/replies/:replyId/softDelete` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/soft-delete-channel-message-reply.md) for the provider-specific parameters and requirements.

