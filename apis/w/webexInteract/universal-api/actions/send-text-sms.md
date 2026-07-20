# Webex Interact: Send text SMS

Sends an SMS message from Webex Interact.

```
POST https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/send-text-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/send-text-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message_body": "string",
  "from": "string",
  "to": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/send-text-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message_body": "string",
    "from": "string",
    "to": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `global_merge_fields` | object | no | Global merge fields applied to all recipients unless overridden per recipient. |
| `message_body` | string | yes | SMS message content. Required unless template ID is provided. |
| `name` | string | no | External request name returned in webhooks. |
| `schedule_at` | string | no | Future ISO 8601 date/time for scheduled sending. |
| `valid_until` | string | no | ISO 8601 expiry time for delivery validity. |
| `from` | string | yes | Sender ID for the SMS message. Sender names must already exist in Webex Interact. |
| `to` | list<object> | yes | Array of destination objects containing recipient phone arrays and optional merge fields. |
| `skip_optout_check` | boolean | no | Bypass opt-out checks when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "messages": [
        {}
      ],
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `messages` | array<object> |  |
| `request_id` | string |  |

## Native endpoint

Through the native Webex Interact API, this operation is `POST /v1/sms` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-text-sms.md) for the provider-specific parameters and requirements.

