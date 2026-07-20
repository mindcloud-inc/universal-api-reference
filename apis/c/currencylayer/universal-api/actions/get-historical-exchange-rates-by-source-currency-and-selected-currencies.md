# Currencylayer: Get Historical Exchange Rates By Source Currency And Selected Currencies

Retrieves historical exchange rates by source and selected currencies from Currencylayer on a date.

```
GET https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/get-historical-exchange-rates-by-source-currency-and-selected-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currencylayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/get-historical-exchange-rates-by-source-currency-and-selected-currencies?connectionId=$CONNECTION_ID&date=string&source=string&currencies=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "source": "string",
  "currencies": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/get-historical-exchange-rates-by-source-currency-and-selected-currencies?${params}`, {
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
| `date` | string | yes | Date to retrieve historical rates for, in YYYY-MM-DD format. |
| `source` | string | yes | 3-letter source currency code. |
| `currencies` | string | yes | Comma-separated 3-letter currency codes to limit the returned rates. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Currencylayer API returns.

## Native endpoint

Through the native Currencylayer API, this operation is `GET /historical` (base URL `https://api.currencylayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-exchange-rates-by-source-currency-and-selected-currencies.md) for the provider-specific parameters and requirements.

