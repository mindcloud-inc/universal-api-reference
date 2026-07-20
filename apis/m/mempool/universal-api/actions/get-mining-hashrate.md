# Mempool: Get Mining Hashrate

Retrieves network hashrate and difficulty from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mining-hashrate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mining-hashrate?connectionId=$CONNECTION_ID&time_period=3d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "time_period": "3d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mining-hashrate?${params}`, {
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
| `time_period` | string | yes | Hashrate aggregation period, such as 3d, 1w, 1m, 3m, 6m, or 1y. Default: `3d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentDifficulty": 1,
      "currentHashrate": 1,
      "difficulty": [
        {}
      ],
      "hashrates": [
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
| `currentDifficulty` | number |  |
| `currentHashrate` | number |  |
| `difficulty` | array<object> |  |
| `hashrates` | array<object> |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /v1/mining/hashrate/[:time_period]` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mining-hashrate.md) for the provider-specific parameters and requirements.

