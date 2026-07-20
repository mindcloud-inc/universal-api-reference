# D7 Messaging: Send Viber Message

Sends a Viber message through D7 Messaging.

```
POST https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-viber-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-viber-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageGlobals.originator": "string",
  "messages[0].recipients[]": [
    "string"
  ],
  "messages[0].content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-viber-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageGlobals.originator": "string",
    "messages[0].recipients[]": ["string"],
    "messages[0].content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageGlobals.originator` | string | yes | Sender name shown to the recipient in Viber. |
| `messages[0].recipients[]` | array<string> | yes | One or more Viber recipient mobile numbers in E.164 format including country code. |
| `messages[0].content` | string | yes | Viber message body. |
| `messages[0].label` | string | no | Viber message category such as PROMOTION. Default: `PROMOTION`. |
| `messageGlobals.callbackUrl` | string | no | Webhook URL to receive delivery callbacks for this Viber message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "request_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `request_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native D7 Messaging API, this operation is `POST /viber/v1/send` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-viber-message.md) for the provider-specific parameters and requirements.

