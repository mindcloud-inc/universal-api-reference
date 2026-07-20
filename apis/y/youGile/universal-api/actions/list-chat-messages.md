# YouGile: List chat messages

Retrieves chat messages from a YouGile chat.

```
GET https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouGile `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-chat-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-chat-messages?${params}`, {
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
| `chatId` | string | yes | The YouGile chat ID. |
| `includeDeleted` | boolean | no | Include deleted messages in the result. |
| `fromUserId` | string | no | Filter messages by sender user ID. |
| `text` | string | no | Filter messages by text. |
| `label` | string | no | Filter messages by label. |
| `since` | number | no | Return messages updated since this timestamp. |
| `includeSystem` | boolean | no | Include system messages in the result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {}
      ],
      "paging": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array<object> |  |
| `paging` | object |  |

## Native endpoint

Through the native YouGile API, this operation is `GET /chats/:chatId/messages` (base URL `{{credentials.companyDomain}}/api-v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chat-messages.md) for the provider-specific parameters and requirements.

