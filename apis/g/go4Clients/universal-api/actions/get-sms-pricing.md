# Go4Clients: Get SMS Pricing

Retrieves SMS pricing details from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-sms-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-sms-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-sms-pricing?${params}`, {
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
      "country": "string",
      "currency": {
        "alphabeticCode": "string",
        "currencyName": "Ava Chen",
        "entity": "string",
        "exchangeRatePerUsd": 1,
        "numericCode": "string"
      },
      "description": "string",
      "endDate": "string",
      "mcc": "string",
      "mccMncId": 1,
      "mnc": "string",
      "name": "Ava Chen",
      "network": "string",
      "productType": "string",
      "rate": 1,
      "rateDeckId": 1,
      "rateId": 1,
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
| `country` | string |  |
| `currency.alphabeticCode` | string |  |
| `currency.currencyName` | string |  |
| `currency.entity` | string |  |
| `currency.exchangeRatePerUsd` | number |  |
| `currency.numericCode` | string |  |
| `description` | string |  |
| `endDate` | string |  |
| `mcc` | string |  |
| `mccMncId` | number |  |
| `mnc` | string |  |
| `name` | string |  |
| `network` | string |  |
| `productType` | string |  |
| `rate` | number |  |
| `rateDeckId` | number |  |
| `rateId` | number |  |
| `startDate` | string |  |
| `volume` | number |  |

## Native endpoint

Through the native Go4Clients API, this operation is `GET /api/pricing/v1.0/sms` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-pricing.md) for the provider-specific parameters and requirements.

