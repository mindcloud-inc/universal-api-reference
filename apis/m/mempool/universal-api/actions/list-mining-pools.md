# Mempool: List Mining Pools

Retrieves mining pools from Mempool for a time period.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-mining-pools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-mining-pools?connectionId=$CONNECTION_ID&time_period=1w" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "time_period": "1w"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-mining-pools?${params}`, {
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
| `time_period` | string | yes | Mining pool aggregation period, such as 1w, 1m, 3m, 6m, or 1y. Default: `1w`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockCount": 1,
      "lastEstimatedHashrate": 1,
      "lastEstimatedHashrate1w": 1,
      "lastEstimatedHashrate3d": 1,
      "pools": [
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
| `blockCount` | number |  |
| `lastEstimatedHashrate` | number |  |
| `lastEstimatedHashrate1w` | number |  |
| `lastEstimatedHashrate3d` | number |  |
| `pools` | array<object> |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /v1/mining/pools/[:time_period]` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mining-pools.md) for the provider-specific parameters and requirements.

