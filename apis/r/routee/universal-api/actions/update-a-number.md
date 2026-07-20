# Routee: Update a Number

Updates an existing number in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-a-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-a-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msisdn": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-a-number', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msisdn": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msisdn` | string | yes | The phone number in E.164 format, without the '+' sign before the country code e.g., 447403940655. |
| `inboundSmsCallbackUrl` | string | no | Defines the callback URL that will receive the inbound messages. |
| `voiceInboundStrategy` | object | no | Defines the Voice inbound strategy |
| `voiceInboundStrategy.dialplanUrl` | string | no | Defines the dialplan URL |
| `inboundVoiceCallbackUrl` | string | no | Defines the callback URL that will receive the inbound Voice messages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activationCosts": [
        [
          {}
        ]
      ],
      "country": "string",
      "inboundCosts": [
        [
          {}
        ]
      ],
      "inboundSmsCallbackUrl": "https://example.com",
      "inboundVoiceCallbackUrl": "https://example.com",
      "monthlyCosts": [
        [
          {}
        ]
      ],
      "msisdn": "string",
      "nextRenewal": "string",
      "services": [
        [
          "string"
        ]
      ],
      "trackingId": "string",
      "voiceInboundStrategy": {
        "dialplanUrl": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activationCosts[]` | array<object> |  |
| `activationCosts[].currency` | string |  |
| `activationCosts[].price` | number |  |
| `country` | string |  |
| `inboundCosts[]` | array<object> |  |
| `inboundCosts[].currency` | string |  |
| `inboundCosts[].price` | number |  |
| `inboundCosts[].service` | string |  |
| `inboundSmsCallbackUrl` | string |  |
| `inboundVoiceCallbackUrl` | string |  |
| `monthlyCosts[]` | array<object> |  |
| `monthlyCosts[].currency` | string |  |
| `monthlyCosts[].price` | number |  |
| `msisdn` | string |  |
| `nextRenewal` | string |  |
| `services[]` | array<string> |  |
| `trackingId` | string |  |
| `voiceInboundStrategy` | object |  |
| `voiceInboundStrategy.dialplanUrl` | string |  |

## Native endpoint

Through the native Routee API, this operation is `PUT /numbers/my/:msisdn` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-number.md) for the provider-specific parameters and requirements.

