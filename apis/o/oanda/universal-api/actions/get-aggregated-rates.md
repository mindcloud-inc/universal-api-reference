# Oanda: Get Aggregated Rates

Retrieves aggregated candle rates from Oanda.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-aggregated-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-aggregated-rates?connectionId=$CONNECTION_ID&base=EUR&end_time=2025-04-10T13%3A00%3A00%2B00%3A00&ext=json&start_time=2025-04-10T12%3A00%3A00%2B00%3A00" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "base": "EUR",
  "end_time": "2025-04-10T13:00:00+00:00",
  "ext": "json",
  "start_time": "2025-04-10T12:00:00+00:00"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-aggregated-rates?${params}`, {
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
| `base` | string | yes | Base currency or comma-separated list. Default: `EUR`. |
| `data_set` | string | no | Dataset code. |
| `decimal_places` | string | no | Decimal precision or all. |
| `end_time` | string | yes | ISO 8601 end timestamp on a 15-minute boundary. Default: `2025-04-10T13:00:00+00:00`. |
| `ext` | string | yes | Response format. Default: `json`. |
| `fields` | string | no | Comma-separated response fields. |
| `interbank` | string | no | Interbank pricing multiplier. |
| `quote` | string | no | Quote currency or comma-separated list. |
| `start_time` | string | yes | ISO 8601 start timestamp on a 15-minute boundary. Default: `2025-04-10T12:00:00+00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "quotes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Request metadata and effective parameters. |
| `quotes` | array<object> | Aggregated candle quotes. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v2/rates/aggregated.:ext` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aggregated-rates.md) for the provider-specific parameters and requirements.

