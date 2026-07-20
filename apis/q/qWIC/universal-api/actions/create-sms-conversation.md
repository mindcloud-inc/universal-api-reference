# QWIC: Create SMS Conversation

Creates an SMS conversation in QWIC.

```
POST https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/create-sms-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/create-sms-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": {},
  "message": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/create-sms-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": {},
    "message": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Configured SMS sender number. |
| `to` | object | yes | Recipient contact object with phone and optional name/email. |
| `message` | object | yes | SMS message object. QWIC docs show text payloads for this endpoint. |
| `assignee` | string | no | Optional agent email to assign the new conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native QWIC API, this operation is `POST /v1/conversations` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sms-conversation.md) for the provider-specific parameters and requirements.

