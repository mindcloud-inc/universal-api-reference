# Blockscout: Get Address Counters

Retrieves activity counters for an address from Blockscout.

```
GET https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-address-counters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blockscout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-address-counters?connectionId=$CONNECTION_ID&address_hash_param=0xfFd12B32d000617551681973911Fd3ad49B89294" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address_hash_param": "0xfFd12B32d000617551681973911Fd3ad49B89294"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-address-counters?${params}`, {
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
| `chain_id` | string | no | Blockscout chain ID, for example 10 for Optimism. Default: `10`. |
| `address_hash_param` | string | yes | Address hash to retrieve counters for. Default: `0xfFd12B32d000617551681973911Fd3ad49B89294`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "token_transfers_count": 1,
      "transactions_count": 1,
      "validations_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token_transfers_count` | number |  |
| `transactions_count` | number |  |
| `validations_count` | number |  |

## Native endpoint

Through the native Blockscout API, this operation is `GET /:chain_id/api/v2/addresses/:address_hash_param/counters` (base URL `https://api.blockscout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address-counters.md) for the provider-specific parameters and requirements.

