# Seven: Get Active Number

Retrieves an active number from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-active-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-active-number?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-active-number?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | string | yes | The phone number to get details for. |

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
          "number": [
            "string"
          ]
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
| `forward_sms_mo.sms.number` | array<string> |  |
| `friendly_name` | string |  |
| `number` | string |  |

## Native endpoint

Through the native Seven API, this operation is `GET /numbers/active/:number` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-active-number.md) for the provider-specific parameters and requirements.

