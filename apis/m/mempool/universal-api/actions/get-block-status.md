# Mempool: Get Block Status

Retrieves the confirmation status of a block from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block-status?connectionId=$CONNECTION_ID&hash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block-status?${params}`, {
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
      "height": 1,
      "in_best_chain": true,
      "next_best": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `height` | number |  |
| `in_best_chain` | boolean |  |
| `next_best` | string |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /block/[:hash]/status` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-status.md) for the provider-specific parameters and requirements.

