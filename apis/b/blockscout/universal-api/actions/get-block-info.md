# Blockscout: Get Block Info

Retrieves details for a specific block from Blockscout.

```
GET https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-block-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blockscout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-block-info?connectionId=$CONNECTION_ID&block_hash_or_number_param=150722206" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "block_hash_or_number_param": "150722206"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-block-info?${params}`, {
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
| `chain_id` | string | no | Default: `10`. |
| `block_hash_or_number_param` | string | yes | Block number or hash to retrieve. Default: `150722206`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hash": "string",
      "height": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "transactions_count": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hash` | string |  |
| `height` | number |  |
| `timestamp` | date |  |
| `transactions_count` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Blockscout API, this operation is `GET /:chain_id/api/v2/blocks/:block_hash_or_number_param` (base URL `https://api.blockscout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-info.md) for the provider-specific parameters and requirements.

