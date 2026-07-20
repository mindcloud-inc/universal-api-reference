# boomApp Connect: Make Voice Call

Creates a text-to-speech voice call in boomApp Connect.

```
POST https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/make-voice-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a boomApp Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/make-voice-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voice_intro": "Intro message",
  "message_content": "Voice message text",
  "recipient_address[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/make-voice-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voice_intro": "Intro message",
    "message_content": "Voice message text",
    "recipient_address[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voice_intro` | string | yes | Welcome message played when the call is answered. Required for successful runtime submission. Example: `Intro message`. |
| `message_content` | string | yes | Main voice message body. Required for successful runtime submission. Example: `Voice message text`. |
| `recipient_address[]` | array<object> | yes | Recipient phone numbers as objects with a number field. Required for successful runtime submission. Example: `[object Object]`. |
| `voice_thank_you` | string | no | Exit message played after the recipient listens or responds. |
| `voice_retries` | number | no | Retry attempts, maximum 3 per connector schema. |
| `voice_delay` | number | no | Interval between retry attempts in minutes. |
| `email_responses` | string | no | Email address to forward response details. |
| `push_responses` | string | no | Webhook to push response details. |
| `unique_identifier` | string | no | Customer-side dedupe identifier. |
| `locale` | string | no | Voice locale, accent, or language. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1,
      "transactions": {
        "boomerangId": "string",
        "partsPerMessage": 1,
        "telephoneNumber": "string",
        "transactionId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Response message. |
| `status` | number | Response status code. |
| `transactions` | array<object> | Outbound voice transaction results. |
| `transactions.boomerangId` | string | Boomerang message ID. |
| `transactions.partsPerMessage` | number | Parts per message. |
| `transactions.telephoneNumber` | string | Recipient telephone number. |
| `transactions.transactionId` | string | Boomerang transaction ID. |

## Native endpoint

Through the native boomApp Connect API, this operation is `POST /v1/flat/voice` (base URL `https://direct-api.apps.boomcomms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/make-voice-call.md) for the provider-specific parameters and requirements.

