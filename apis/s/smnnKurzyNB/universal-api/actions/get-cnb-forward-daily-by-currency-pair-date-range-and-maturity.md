# Směnné kurzy ČNB: Get CNB Forward Daily by Currency Pair, Date Range, and Maturity

Retrieves forward rates by currency pair, date range, and maturity from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-forward-daily-by-currency-pair-date-range-and-maturity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-forward-daily-by-currency-pair-date-range-and-maturity?connectionId=$CONNECTION_ID&currencyPair=USD_TO_CZK&dateFrom=2026-04-01&maturity=THREE_MONTH" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "currencyPair": "USD_TO_CZK",
  "dateFrom": "2026-04-01",
  "maturity": "THREE_MONTH"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-forward-daily-by-currency-pair-date-range-and-maturity?${params}`, {
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
| `currencyPair` | string | yes | One of: `ALL`, `EUR_TO_CZK`, `USD_TO_CZK`. Example: `USD_TO_CZK`. |
| `dateFrom` | date | yes | Example: `2026-04-01`. |
| `dateTo` | date | no | Example: `2026-04-30`. |
| `maturity` | string | yes | One of: `ALL`, `SIX_MONTH`, `THREE_MONTH`. Example: `THREE_MONTH`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "forwardPoints": [
        {
          "ccyPair": "string",
          "forwardPoints": 1,
          "maturity": "string",
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
| `forwardPoints[].ccyPair` | string |  |
| `forwardPoints[].forwardPoints` | number |  |
| `forwardPoints[].maturity` | string |  |
| `forwardPoints[].validFor` | string |  |

## Native endpoint

Through the native Směnné kurzy ČNB API, this operation is `GET /forward/daily-range-currency-pair-maturity` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnb-forward-daily-by-currency-pair-date-range-and-maturity.md) for the provider-specific parameters and requirements.

