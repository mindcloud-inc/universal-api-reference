# Mempool: Get Mining Pool

Retrieves mining pool details from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mining-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mining-pool?connectionId=$CONNECTION_ID&slug=foundryusa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "foundryusa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mining-pool?${params}`, {
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
| `slug` | string | yes | Mempool mining pool slug, such as foundryusa. Default: `foundryusa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avgBlockHealth": 1,
      "blockCount": {},
      "blockShare": {},
      "estimatedHashrate": 1,
      "pool": {},
      "reportedHashrate": 1,
      "totalReward": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgBlockHealth` | number |  |
| `blockCount` | object |  |
| `blockShare` | object |  |
| `estimatedHashrate` | number |  |
| `pool` | object |  |
| `reportedHashrate` | number |  |
| `totalReward` | string |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /v1/mining/pool/[:slug]` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mining-pool.md) for the provider-specific parameters and requirements.

