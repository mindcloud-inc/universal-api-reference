# Routee: Rent a Number

Rents a new number in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/rent-a-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/rent-a-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msisdn": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/rent-a-number', {
  method: 'POST',
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
| `msisdn` | string | yes | The phone number. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). |
| `inboundSmsCallbackUrl` | string | no | Defines the callback URL that will receive the inbound messages. |
| `voiceInboundStrategy` | object | no | Defines the Voice inbound strategy |
| `voiceInboundStrategy.dialplanUrl` | string | no | Defines the dialplan URL |
| `voiceInboundStrategy.forwardCallToSip` | string | no | A valid SIP address to forward the inbound call |
| `voiceInboundStrategy.forwardCallTo` | string | no | A valid phone number in E.164 Format to forward the inbound call |
| `inboundVoiceCallbackUrl` | string | no | Defines the callback URL that will receive the inbound Voice messages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activationCosts": {
        "currency": "string",
        "price": 1
      },
      "chargeInterval": 1,
      "country": "string",
      "inboundCosts": [
        [
          {}
        ]
      ],
      "inboundSmsCallbackUrl": "https://example.com",
      "monthlyCosts": {
        "currency": "string",
        "price": 1
      },
      "msisdn": "string",
      "nextRenewal": "string",
      "services": [
        [
          "string"
        ]
      ],
      "tollFree": true,
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activationCosts` | object |  |
| `activationCosts.currency` | string |  |
| `activationCosts.price` | number |  |
| `chargeInterval` | number |  |
| `country` | string |  |
| `inboundCosts[]` | array<object> |  |
| `inboundCosts[].currency` | string |  |
| `inboundCosts[].price` | number |  |
| `inboundCosts[].service` | string |  |
| `inboundSmsCallbackUrl` | string |  |
| `monthlyCosts` | object |  |
| `monthlyCosts.currency` | string |  |
| `monthlyCosts.price` | number |  |
| `msisdn` | string |  |
| `nextRenewal` | string |  |
| `services[]` | array<string> |  |
| `tollFree` | boolean |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /numbers/my` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rent-a-number.md) for the provider-specific parameters and requirements.

