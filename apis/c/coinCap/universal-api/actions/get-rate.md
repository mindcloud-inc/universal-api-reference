# CoinCap: Get Rate

Retrieves a conversion rate from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-rate?connectionId=$CONNECTION_ID&slug=united-states-dollar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "united-states-dollar"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-rate?${params}`, {
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
| `slug` | string | yes | The rate slug to retrieve. Example: `united-states-dollar`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currencySymbol": "string",
      "id": "string",
      "rateUsd": "string",
      "symbol": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencySymbol` | string |  |
| `id` | string |  |
| `rateUsd` | string |  |
| `symbol` | string |  |
| `type` | string |  |

## Native endpoint

Through the native CoinCap API, this operation is `GET /rates/:slug` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rate.md) for the provider-specific parameters and requirements.

