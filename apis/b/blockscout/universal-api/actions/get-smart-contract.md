# Blockscout: Get Smart Contract

Retrieves details for a smart contract from Blockscout.

```
GET https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-smart-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blockscout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-smart-contract?connectionId=$CONNECTION_ID&address_hash_param=0x4200000000000000000000000000000000000011" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address_hash_param": "0x4200000000000000000000000000000000000011"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-smart-contract?${params}`, {
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
| `address_hash_param` | string | yes | Smart contract address. Default: `0x4200000000000000000000000000000000000011`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_hash": "string",
      "compiler_version": "string",
      "language": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_hash` | string |  |
| `compiler_version` | string |  |
| `language` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Blockscout API, this operation is `GET /:chain_id/api/v2/smart-contracts/:address_hash_param` (base URL `https://api.blockscout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smart-contract.md) for the provider-specific parameters and requirements.

