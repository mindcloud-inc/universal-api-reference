# JetAPI: Create Delivery

Creates a new message delivery in JetAPI.

```
POST https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "995598464533",
  "text": "Test message"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-delivery', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "995598464533",
    "text": "Test message"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | yes | Recipient phone number in international format. Example: `995598464533`. |
| `text` | string | yes | Message text. Example: `Test message`. |
| `senderName` | string | no | Example: `InfoSMS`. |
| `utmMark` | string | no | Example: `campaign_mark`. |
| `callbackUrl` | string | no | Status callback URL. Example: `https://example.com/webhook`. |
| `externalId` | string | no | Client-side idempotency key. Example: `client-message-1`. |
| `dispatchRouting[]` | array<string> | no | Example: `whatsapp,tdlib`. |
| `scheduledAt` | date | no | UTC datetime in YYYY-MM-DD HH:MM:SS. Example: `2026-04-01 12:00:00`. |
| `priority` | string | no | high, medium, or low. Default: `medium`. Example: `high`. |
| `username` | string | no | Example: `@username`. |
| `replyToMessageId` | string | no | Example: `123456`. |
| `tdlibUserId` | string | no | Example: `-100123456`. |
| `simulateTyping` | boolean | no | Whether to simulate typing before sending on WhatsApp. Default: `true`. |
| `whatsappLid` | string | no | Example: `43445322325@lid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "dispatchRouting": [
        "string"
      ],
      "externalId": "string",
      "id": 1,
      "phone": "string",
      "priority": "string",
      "replyToMessageId": "string",
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "senderName": "Ava Chen",
      "simulateTyping": true,
      "statusDescription": "string",
      "statusId": 1,
      "sum": "string",
      "totalSms": 1,
      "trafficCategory": 1,
      "utmMark": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `dispatchRouting` | array<string> |  |
| `externalId` | string |  |
| `id` | number |  |
| `phone` | string |  |
| `priority` | string |  |
| `replyToMessageId` | string |  |
| `scheduledAt` | date |  |
| `senderName` | string |  |
| `simulateTyping` | boolean |  |
| `statusDescription` | string |  |
| `statusId` | number |  |
| `sum` | string |  |
| `totalSms` | number |  |
| `trafficCategory` | number |  |
| `utmMark` | string |  |

## Native endpoint

Through the native JetAPI API, this operation is `POST /api/v1/delivery` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-delivery.md) for the provider-specific parameters and requirements.

