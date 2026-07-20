# Minerstat: List Coins

Retrieves coins from the Minerstat catalog.

```
GET https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-coins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minerstat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-coins?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-coins?${params}`, {
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
| `list` | string | no | Comma-separated coin tickers like BTC,BCH,BSV. Example: `BTC,BCH,BSV`. |
| `algo` | string | no | Comma-separated algorithms like SHA-256,Scrypt. Example: `SHA-256,Scrypt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "algorithm": "string",
      "coin": "string",
      "difficulty": 1,
      "id": "string",
      "name": "Ava Chen",
      "network_hashrate": 1,
      "price": 1,
      "reward": 1,
      "reward_block": 1,
      "reward_unit": "string",
      "type": "string",
      "updated": 1,
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `algorithm` | string |  |
| `coin` | string |  |
| `difficulty` | number |  |
| `id` | string |  |
| `name` | string |  |
| `network_hashrate` | number |  |
| `price` | number |  |
| `reward` | number |  |
| `reward_block` | number |  |
| `reward_unit` | string |  |
| `type` | string |  |
| `updated` | number |  |
| `volume` | number |  |

## Native endpoint

Through the native Minerstat API, this operation is `GET /v2/coins` (base URL `https://api.minerstat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-coins.md) for the provider-specific parameters and requirements.

