# Messaggio: Send Viber Text + Button

Creates a Viber text message with a button in Messaggio.

```
POST https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-viber-text-button
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Messaggio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-viber-text-button" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientPhone": "string",
  "senderCode": "string",
  "messageLabel": "string",
  "messageText": "string",
  "buttonText": "string",
  "buttonUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-viber-text-button', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientPhone": "string",
    "senderCode": "string",
    "messageLabel": "string",
    "messageText": "string",
    "buttonText": "string",
    "buttonUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientPhone` | string | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | string | yes | Viber sender code from the Messaggio project. |
| `messageLabel` | string | yes | Viber message label. Use promotion or transaction. |
| `messageText` | string | yes | Viber message text. |
| `buttonText` | string | yes | Viber button caption. |
| `buttonUrl` | string | yes | URL to open when the Viber button is pressed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accepted_at": "string",
      "messages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted_at` | string | Timestamp when Messaggio accepted the send request. |
| `messages` | array<object> | Per-recipient send results returned by Messaggio, including recipient, message_id, or error. |

## Native endpoint

Through the native Messaggio API, this operation is `POST /send` (base URL `https://msg.messaggio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-viber-text-button.md) for the provider-specific parameters and requirements.

