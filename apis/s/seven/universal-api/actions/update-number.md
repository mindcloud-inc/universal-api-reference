# Seven: Update Number

Updates an active number in Seven.

```
PUT https://connect.mindcloud.co/v1/universal/seven/latest/actions/update-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seven/latest/actions/update-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/update-number', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | string | yes | The phone number to update details for. |
| `friendlyName` | string | no | The updated friendly name for the number. |
| `smsForward[]` | array<string> | no | The phone number to forward incoming SMS to. If empty, incoming SMS won&#x27;t be forwarded by SMS. |
| `emailForward[]` | array<string> | no | The email address to forward incoming SMS to. If empty, incoming SMS won&#x27;t be forwarded by email. |
| `slackForward` | string | no | The Slack webhook URL to forward incoming SMS to. If empty, incoming SMS won&#x27;t be forwarded by Slack. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing": {
        "fees": {
          "basic_charge": 1,
          "setup": 1,
          "sms_mo": 1,
          "voice_mo": 1
        },
        "payment_interval": "string"
      },
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "expires": "string",
      "features": {
        "a2p_sms": true,
        "sms": true,
        "voice": true
      },
      "forward_sms_mo": {
        "email": {
          "address": [
            "ava@example.com"
          ],
          "enabled": true
        },
        "slack": {
          "enabled": true,
          "uri": "string"
        },
        "sms": {
          "enabled": true,
          "number": "string"
        }
      },
      "friendly_name": "Ava Chen",
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing` | object |  |
| `billing.fees` | object |  |
| `billing.fees.basic_charge` | number |  |
| `billing.fees.setup` | number |  |
| `billing.fees.sms_mo` | number |  |
| `billing.fees.voice_mo` | number |  |
| `billing.payment_interval` | string |  |
| `country` | string |  |
| `created` | date |  |
| `expires` | string |  |
| `features` | object |  |
| `features.a2p_sms` | boolean |  |
| `features.sms` | boolean |  |
| `features.voice` | boolean |  |
| `forward_sms_mo` | object |  |
| `forward_sms_mo.email` | object |  |
| `forward_sms_mo.email.address` | array<string> |  |
| `forward_sms_mo.email.enabled` | boolean |  |
| `forward_sms_mo.slack` | object |  |
| `forward_sms_mo.slack.enabled` | boolean |  |
| `forward_sms_mo.slack.uri` | string |  |
| `forward_sms_mo.sms` | object |  |
| `forward_sms_mo.sms.enabled` | boolean |  |
| `forward_sms_mo.sms.number` | string |  |
| `friendly_name` | string |  |
| `number` | string |  |

## Native endpoint

Through the native Seven API, this operation is `PATCH /numbers/active/:number` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-number.md) for the provider-specific parameters and requirements.

