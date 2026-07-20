# boomApp Connect: Send SMS One-Way

Creates a one-way SMS message in boomApp Connect.

```
POST https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/send-sms-one-way
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a boomApp Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/send-sms-one-way" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "MindCloud",
  "message_content": "Message text",
  "recipient_address[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/send-sms-one-way', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "MindCloud",
    "message_content": "Message text",
    "recipient_address[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Originating ID for the one-way SMS message. Required for successful runtime submission. Example: `MindCloud`. |
| `message_content` | string | yes | Outbound SMS message content. Required for successful runtime submission. Example: `Message text`. |
| `recipient_address[]` | array<object> | yes | Recipient mobile numbers as objects with a number field. Required for successful runtime submission. Example: `[object Object]`. |
| `priority` | boolean | no | Set true to override Social Hours when the account supports it. |
| `unique_identifier` | string | no | Customer-side dedupe identifier. |
| `campaign_name` | string | no | Optional campaign grouping name. |
| `custom_parameter` | string | no | Optional custom reference value. |

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
| `transactions` | array<object> | Outbound message transaction results. |
| `transactions.boomerangId` | string | Boomerang message ID. |
| `transactions.partsPerMessage` | number | Parts per message. |
| `transactions.telephoneNumber` | string | Recipient telephone number. |
| `transactions.transactionId` | string | Boomerang transaction ID. |

## Native endpoint

Through the native boomApp Connect API, this operation is `POST /v1/flat/sms1` (base URL `https://direct-api.apps.boomcomms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-one-way.md) for the provider-specific parameters and requirements.

