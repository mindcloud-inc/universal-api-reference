# Usedesk: Create Chat

Creates a new chat in Usedesk.

```
POST https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "channelId": 1,
  "message.text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "channelId": 1,
    "message.text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | no | Existing chat ID. Omit to create a new chat. |
| `companyId` | number | yes | Your company ID. |
| `message.from.clientId` | string | no | Client ID bound to the chat. |
| `message.from.email` | string | no | Client email. |
| `message.from.name` | string | no | Client name. |
| `channelId` | number | yes | Chat channel ID. |
| `message.text` | string | yes | Message text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel_id": 1,
      "chat_id": 1,
      "client_id": 1,
      "company_id": 1,
      "ticket_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel_id` | number |  |
| `chat_id` | number |  |
| `client_id` | number |  |
| `company_id` | number |  |
| `ticket_id` | number |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /chat/addMessage` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat.md) for the provider-specific parameters and requirements.

