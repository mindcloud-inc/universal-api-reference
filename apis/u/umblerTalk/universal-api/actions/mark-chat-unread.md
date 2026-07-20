# Umbler Talk: Mark Chat Unread

Marks a chat as unread in Umbler Talk.

```
PUT https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/mark-chat-unread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/mark-chat-unread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/mark-chat-unread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The chat ID. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "channel": {},
      "contact": {},
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "hasMessagesBeforeAllowedHistory": true,
      "id": "string",
      "lastMessage": {},
      "latestMessages": [
        {}
      ],
      "open": true,
      "organization": {},
      "private": true,
      "sector": {},
      "tags": [
        {}
      ],
      "waiting": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `channel` | object |  |
| `contact` | object |  |
| `createdAtUTC` | date |  |
| `hasMessagesBeforeAllowedHistory` | boolean |  |
| `id` | string |  |
| `lastMessage` | object |  |
| `latestMessages` | array<object> |  |
| `open` | boolean |  |
| `organization` | object |  |
| `private` | boolean |  |
| `sector` | object |  |
| `tags` | array<object> |  |
| `waiting` | boolean |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `PUT /v1/chats/[:id]/unread/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-chat-unread.md) for the provider-specific parameters and requirements.

