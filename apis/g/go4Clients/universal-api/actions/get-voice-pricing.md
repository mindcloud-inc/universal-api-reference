# Go4Clients: Get Voice Pricing

Retrieves voice pricing details from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-voice-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-voice-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-voice-pricing?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "billingIncrementInSeconds": 1,
      "country": "string",
      "countryCode": "string",
      "currency": {
        "alphabeticCode": "string",
        "currencyName": "Ava Chen",
        "entity": "string",
        "exchangeRatePerUsd": 1,
        "numericCode": "string"
      },
      "description": "string",
      "endDate": "string",
      "gracePeriod": 1,
      "minimumBillingTime": 1,
      "name": "Ava Chen",
      "network": "string",
      "prefix": "string",
      "productType": "string",
      "rate": 1,
      "rateDeckId": 1,
      "rateId": 1,
      "ratePerMinute": 1,
      "startDate": "string",
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingIncrementInSeconds` | number |  |
| `country` | string |  |
| `countryCode` | string |  |
| `currency.alphabeticCode` | string |  |
| `currency.currencyName` | string |  |
| `currency.entity` | string |  |
| `currency.exchangeRatePerUsd` | number |  |
| `currency.numericCode` | string |  |
| `description` | string |  |
| `endDate` | string |  |
| `gracePeriod` | number |  |
| `minimumBillingTime` | number |  |
| `name` | string |  |
| `network` | string |  |
| `prefix` | string |  |
| `productType` | string |  |
| `rate` | number |  |
| `rateDeckId` | number |  |
| `rateId` | number |  |
| `ratePerMinute` | number |  |
| `startDate` | string |  |
| `volume` | number |  |

## Native endpoint

Through the native Go4Clients API, this operation is `GET /api/pricing/v1.0/voice` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voice-pricing.md) for the provider-specific parameters and requirements.

