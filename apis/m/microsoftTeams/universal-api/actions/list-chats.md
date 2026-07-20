# Microsoft Teams: List Chats

Retrieves chats from Microsoft Teams.

```
GET https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-chats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-chats?${params}`, {
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

Through the native Microsoft Teams API, this operation is `GET /v1.0/me/chats` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

