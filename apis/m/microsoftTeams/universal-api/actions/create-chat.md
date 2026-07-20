# Microsoft Teams: Create Chat

Creates a new chat in Microsoft Teams.

```
POST https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/create-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatType": "string",
  "members[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatType": "string",
    "members[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatType` | string | yes | Chat type, for example oneOnOne or group. |
| `members[]` | array<object> | yes | Array of conversation member objects. Include every participant, including the initiating user. Each item should include @odata.type, roles, and user@odata.bind per Microsoft Graph create chat docs. |
| `topic` | string | no | Topic for group chats. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatType": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastUpdatedDateTime": "2026-05-07T12:00:00.000Z",
      "onlineMeetingInfo": {},
      "tenantId": "string",
      "topic": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatType` | string | Type of chat. |
| `createdDateTime` | date | Timestamp at which the chat was created. |
| `id` | string | Unique identifier for the chat. |
| `lastUpdatedDateTime` | date | Timestamp at which the chat was last updated. |
| `onlineMeetingInfo` | object | Meeting information associated with the chat, when present. |
| `tenantId` | string | Microsoft Entra tenant identifier. |
| `topic` | string | Chat title or topic. |
| `webUrl` | string | URL for the chat in Microsoft Teams. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `POST /v1.0/chats` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat.md) for the provider-specific parameters and requirements.

