# Etherscan: Get Historical ERC20-Token TotalSupply by ContractAddress & BlockNo

Retrieves historical ERC20 token total supply by block.

```
GET https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-historical-erc20-token-total-supply-by-contract-address-block-no
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Etherscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-historical-erc20-token-total-supply-by-contract-address-block-no?connectionId=$CONNECTION_ID&contractAddress=string&blockNumber=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractAddress": "string",
  "blockNumber": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-historical-erc20-token-total-supply-by-contract-address-block-no?${params}`, {
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
| `chainId` | string | no | Default: `1`. |
| `contractAddress` | string | yes |  |
| `blockNumber` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Etherscan API, this operation is `GET /v2/api` (base URL `https://api.etherscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-erc20-token-total-supply-by-contract-address-block-no.md) for the provider-specific parameters and requirements.

