# Finnhub: Get Forex Rates

Retrieves forex rates from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-forex-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-forex-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-forex-rates?${params}`, {
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
| `base` | string | no | Optional base currency, such as USD. Example: `e.g. USD`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | no | Exchange-rate date in YYYY-MM-DD format. Example: `2026-04-14`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base": "string",
      "quote": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base` | string |  |
| `quote` | object | Map of currency code to exchange rate. |

## Native endpoint

Through the native Finnhub API, this operation is `GET /forex/rates` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forex-rates.md) for the provider-specific parameters and requirements.

