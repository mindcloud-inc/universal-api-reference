# Mews: Get All Exchange Rates

Retrieves exchange rates from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-exchange-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-exchange-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-exchange-rates?${params}`, {
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
      "enterpriseId": "string",
      "id": "string",
      "sourceCurrency": "string",
      "targetCurrency": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enterpriseId` | string | Enterprise identifier. |
| `id` | string | Unique identifier of the exchange-rate pair. |
| `sourceCurrency` | string | Source currency code. |
| `targetCurrency` | string | Target currency code. |
| `value` | number | Exchange rate value. |

## Native endpoint

Through the native Mews API, this operation is `POST /exchangeRates/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-exchange-rates.md) for the provider-specific parameters and requirements.

