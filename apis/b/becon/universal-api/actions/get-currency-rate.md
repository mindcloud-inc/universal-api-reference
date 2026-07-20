# Becon: Get Currency Rate

Retrieves a cryptocurrency-to-fiat exchange rate from Becon.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-currency-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-currency-rate?connectionId=$CONNECTION_ID&cryptoCurrencyName=Ava%20Chen&currency=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cryptoCurrencyName": "Ava Chen",
  "currency": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-currency-rate?${params}`, {
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
| `cryptoCurrencyName` | string | yes | Crypto currency ISO name, for example btc or bnb. |
| `currency` | string | yes | Target fiat currency ISO name, for example eur or usd. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "price": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `price` | string | Exchange rate value for the requested crypto and fiat pair. |

## Native endpoint

Through the native Becon API, this operation is `GET /v1/currencies/:cryptoCurrencyName` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-currency-rate.md) for the provider-specific parameters and requirements.

