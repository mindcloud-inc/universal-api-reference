# Conexteo: Send Manual SMS

Creates a manual SMS message in Conexteo.

```
POST https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/send-manual-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/send-manual-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "recipients[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/send-manual-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "recipients[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resumeBefore` | boolean | no | Return the required credit summary without sending the SMS campaign. Recommended for safe verification. Default: `true`. |
| `shorturl` | object | no | Optional short URL configuration object with mode and url. |
| `external_id` | string | no | Optional client-provided idempotency key. |
| `scheduleAt` | date | no | Optional UTC ISO-8601 schedule timestamp. |
| `content` | string | yes | SMS message body. |
| `sender` | string | no | Optional sender name, maximum 11 characters. |
| `recipients[]` | array<string> | yes | Array of recipient phone numbers in national or E.164 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_missing": 1,
      "credits_remaining": 1,
      "credits_required": 1,
      "credits_used": 1,
      "doublons": 1,
      "message": "string",
      "message_id": 1,
      "recipients_count": 1,
      "sms_count": 1,
      "stops": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_missing` | number | Missing credits if the campaign cannot be sent. |
| `credits_remaining` | number | Credits still available on the account. |
| `credits_required` | number | Credits required for the campaign when resumeBefore is used. |
| `credits_used` | number | Credits consumed when the message is actually created. |
| `doublons` | number | Duplicate-recipient count. |
| `message` | string | Provider status message. |
| `message_id` | number | Created message identifier when the action is executed without resumeBefore. |
| `recipients_count` | number | Recipient count considered by the provider. |
| `sms_count` | number | Computed SMS segment count. |
| `stops` | number | Recipients excluded because of stop rules. |
| `success` | boolean | Whether the request was accepted by Conexteo. |

## Native endpoint

Through the native Conexteo API, this operation is `POST /messages/sms` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-manual-sms.md) for the provider-specific parameters and requirements.

