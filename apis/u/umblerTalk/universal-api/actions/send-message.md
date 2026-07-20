# Umbler Talk: Send Message

Creates a message in Umbler Talk.

```
POST https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | The chat ID. |
| `message` | string | no | Message text. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "chat": {},
      "contactId": "string",
      "contacts": [
        {}
      ],
      "content": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "eventAtUTC": "2026-05-07T12:00:00.000Z",
      "file": {},
      "fromContact": {},
      "id": "string",
      "isPrivate": true,
      "messageState": "string",
      "messageType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `chat` | object |  |
| `contactId` | string |  |
| `contacts` | array<object> |  |
| `content` | string |  |
| `createdAtUTC` | date |  |
| `eventAtUTC` | date |  |
| `file` | object |  |
| `fromContact` | object |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `messageState` | string |  |
| `messageType` | string |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `POST /v1/messages/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

