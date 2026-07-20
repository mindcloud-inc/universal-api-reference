# CoinCap: Get Asset History

Retrieves historical data for an asset from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-history?connectionId=$CONNECTION_ID&slug=bitcoin&interval=h1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "bitcoin",
  "interval": "h1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-history?${params}`, {
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
| `slug` | string | yes | The asset slug to retrieve history for. Example: `bitcoin`. |
| `interval` | string | yes | The interval to return. Supported values are m1, m5, m15, m30, h1, h2, h6, h12, and d1. Example: `h1`. |
| `start` | number | no | Start timestamp in milliseconds. Example: `1713916800000`. |
| `end` | number | no | End timestamp in milliseconds. Example: `1714003200000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "circulatingSupply": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "priceUsd": "string",
      "time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `circulatingSupply` | number | Runtime field returned by CoinCap history responses. |
| `date` | date |  |
| `priceUsd` | string |  |
| `time` | number |  |

## Native endpoint

Through the native CoinCap API, this operation is `GET /assets/:slug/history` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-history.md) for the provider-specific parameters and requirements.

