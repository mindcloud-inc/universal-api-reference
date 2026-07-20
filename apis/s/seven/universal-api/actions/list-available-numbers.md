# Seven: List Available Numbers

Retrieves available numbers from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-available-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-available-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-available-numbers?${params}`, {
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
| `country` | string | no | The ISO 3166-1 alpha-2 country code of the country to search for available numbers in. |
| `featuresSms` | boolean | no | If set to true , only numbers that support SMS will be returned. |
| `featuresA2pSms` | boolean | no | If set to true , only numbers that support A2P SMS will be returned. |
| `featuresVoice` | boolean | no | If set to true , only numbers that support voice will be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableNumbers": {
        "country": "string",
        "features": {
          "a2p_sms": true,
          "sms": true,
          "voice": true
        },
        "fees": {
          "annually": {
            "basic_charge": 1,
            "setup": 1
          },
          "monthly": {
            "basic_charge": 1,
            "setup": 1
          },
          "sms_mo": 1,
          "voice_mo": 1
        },
        "number": "string",
        "number_parsed": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableNumbers` | array<object> |  |
| `availableNumbers.country` | string |  |
| `availableNumbers.features` | object |  |
| `availableNumbers.features.a2p_sms` | boolean |  |
| `availableNumbers.features.sms` | boolean |  |
| `availableNumbers.features.voice` | boolean |  |
| `availableNumbers.fees` | object |  |
| `availableNumbers.fees.annually` | object |  |
| `availableNumbers.fees.annually.basic_charge` | number |  |
| `availableNumbers.fees.annually.setup` | number |  |
| `availableNumbers.fees.monthly` | object |  |
| `availableNumbers.fees.monthly.basic_charge` | number |  |
| `availableNumbers.fees.monthly.setup` | number |  |
| `availableNumbers.fees.sms_mo` | number |  |
| `availableNumbers.fees.voice_mo` | number |  |
| `availableNumbers.number` | string |  |
| `availableNumbers.number_parsed` | string |  |

## Native endpoint

Through the native Seven API, this operation is `GET /numbers/available` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-numbers.md) for the provider-specific parameters and requirements.

