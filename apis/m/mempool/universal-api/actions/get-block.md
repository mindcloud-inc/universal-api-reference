# Mempool: Get Block

Retrieves details about a block from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block?connectionId=$CONNECTION_ID&hash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block?${params}`, {
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
| `hash` | string | yes | Block hash to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bits": 1,
      "difficulty": 1,
      "extras": {},
      "height": 1,
      "id": "string",
      "mediantime": 1,
      "merkle_root": "string",
      "nonce": 1,
      "previousblockhash": "string",
      "size": 1,
      "stale": true,
      "timestamp": 1,
      "tx_count": 1,
      "version": 1,
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bits` | number |  |
| `difficulty` | number |  |
| `extras` | object |  |
| `height` | number |  |
| `id` | string |  |
| `mediantime` | number |  |
| `merkle_root` | string |  |
| `nonce` | number |  |
| `previousblockhash` | string |  |
| `size` | number |  |
| `stale` | boolean |  |
| `timestamp` | number |  |
| `tx_count` | number |  |
| `version` | number |  |
| `weight` | number |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /block/[:hash]` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block.md) for the provider-specific parameters and requirements.

