# Směnné kurzy ČNB: Get CNB Daily Exchange Rates by Currency and Month

Retrieves daily exchange rates for a currency and month from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-daily-exchange-rates-by-currency-and-month
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-daily-exchange-rates-by-currency-and-month?connectionId=$CONNECTION_ID&currency=USD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "currency": "USD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-daily-exchange-rates-by-currency-and-month?${params}`, {
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
| `yearMonth` | string | no | Example: `2026-04`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rates": [
        {
          "amount": 1,
          "currencyCode": "string",
          "rate": 1,
          "validFor": "string"
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
| `rates[].amount` | number |  |
| `rates[].currencyCode` | string |  |
| `rates[].rate` | number |  |
| `rates[].validFor` | string |  |

## Native endpoint

Through the native Směnné kurzy ČNB API, this operation is `GET /exrates/daily-currency-month` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnb-daily-exchange-rates-by-currency-and-month.md) for the provider-specific parameters and requirements.

