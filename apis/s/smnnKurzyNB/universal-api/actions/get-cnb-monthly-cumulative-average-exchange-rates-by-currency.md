# Směnné kurzy ČNB: Get CNB Monthly Cumulative Average Exchange Rates by Currency

Retrieves monthly cumulative average exchange rates for a currency from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-monthly-cumulative-average-exchange-rates-by-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-monthly-cumulative-average-exchange-rates-by-currency?connectionId=$CONNECTION_ID&currency=USD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "currency": "USD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-monthly-cumulative-average-exchange-rates-by-currency?${params}`, {
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
| `currency` | string | yes | Example: `USD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averages": [
        {
          "amount": 1,
          "average": 1,
          "currencyCode": "string",
          "month": "string",
          "year": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averages[].amount` | number |  |
| `averages[].average` | number |  |
| `averages[].currencyCode` | string |  |
| `averages[].month` | string |  |
| `averages[].year` | number |  |

## Native endpoint

Through the native Směnné kurzy ČNB API, this operation is `GET /exrates/monthly-cumulative-averages-currency` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnb-monthly-cumulative-average-exchange-rates-by-currency.md) for the provider-specific parameters and requirements.

