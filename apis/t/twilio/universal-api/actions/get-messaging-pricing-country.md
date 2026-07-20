# Twilio: Get Messaging Pricing Country

Retrieves messaging pricing for a country from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-messaging-pricing-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-messaging-pricing-country?connectionId=$CONNECTION_ID&isoCountry=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "isoCountry": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-messaging-pricing-country?${params}`, {
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
| `isoCountry` | string | yes | Default: `US`. Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "inboundSmsPrices": [
        {
          "basePrice": "string",
          "currentPrice": "string",
          "numberType": "string"
        }
      ],
      "isoCountry": "string",
      "outboundSmsPrices": [
        {
          "carrier": "string",
          "mcc": "string",
          "mnc": "string",
          "prices": [
            {
              "basePrice": "string",
              "currentPrice": "string",
              "numberType": "string"
            }
          ]
        }
      ],
      "priceUnit": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `inboundSmsPrices[].basePrice` | string |  |
| `inboundSmsPrices[].currentPrice` | string |  |
| `inboundSmsPrices[].numberType` | string |  |
| `isoCountry` | string |  |
| `outboundSmsPrices[].carrier` | string |  |
| `outboundSmsPrices[].mcc` | string |  |
| `outboundSmsPrices[].mnc` | string |  |
| `outboundSmsPrices[].prices[].basePrice` | string |  |
| `outboundSmsPrices[].prices[].currentPrice` | string |  |
| `outboundSmsPrices[].prices[].numberType` | string |  |
| `priceUnit` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `GET https://pricing.twilio.com/v1/Messaging/Countries/:IsoCountry` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-messaging-pricing-country.md) for the provider-specific parameters and requirements.

