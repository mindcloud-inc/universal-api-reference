# CoinCap: Get Asset Market Cap History

Retrieves market cap history for an asset from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-market-cap-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-market-cap-history?connectionId=$CONNECTION_ID&slug=bitcoin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "bitcoin"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-market-cap-history?${params}`, {
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
| `slug` | string | yes | The asset slug to retrieve market cap history for. Example: `bitcoin`. |
| `start` | number | no | Start timestamp in milliseconds. Example: `1713916800000`. |
| `end` | number | no | End timestamp in milliseconds. Example: `1714003200000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "marketCapUsd": "string",
      "time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `marketCapUsd` | string |  |
| `time` | number |  |

## Native endpoint

Through the native CoinCap API, this operation is `GET /assets/:slug/marketcap-history` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-market-cap-history.md) for the provider-specific parameters and requirements.

