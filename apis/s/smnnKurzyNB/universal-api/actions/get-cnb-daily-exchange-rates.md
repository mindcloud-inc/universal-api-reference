# Směnné kurzy ČNB: Get CNB Daily Exchange Rates

Retrieves the last valid daily exchange rates from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-daily-exchange-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-daily-exchange-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-daily-exchange-rates?${params}`, {
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
| `date` | date | no | Example: `2026-04-14`. |
| `lang` | string | no | One of: `CZ`, `EN`. Default: `CZ`. Example: `CZ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rates": [
        {
          "amount": 1,
          "country": "string",
          "currency": "string",
          "currencyCode": "string",
          "order": 1,
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
| `rates[].country` | string |  |
| `rates[].currency` | string |  |
| `rates[].currencyCode` | string |  |
| `rates[].order` | number |  |
| `rates[].rate` | number |  |
| `rates[].validFor` | string |  |

## Native endpoint

Through the native Směnné kurzy ČNB API, this operation is `GET /exrates/daily` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnb-daily-exchange-rates.md) for the provider-specific parameters and requirements.

