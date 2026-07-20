# Etherscan: Get ERC20-Token Account Balance for Token Contract Address

Retrieves an ERC20 token balance for an address.

```
GET https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-erc20-token-account-balance-for-token-contract-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Etherscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-erc20-token-account-balance-for-token-contract-address?connectionId=$CONNECTION_ID&contractAddress=string&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractAddress": "string",
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-erc20-token-account-balance-for-token-contract-address?${params}`, {
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
| `address` | string | yes |  |
| `tag` | string | no | Default: `latest`. |

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
| `message` | string | Etherscan response message. |
| `result` | string | ERC-20 token balance as a decimal string. |
| `status` | string | Etherscan status code. |

## Native endpoint

Through the native Etherscan API, this operation is `GET /v2/api` (base URL `https://api.etherscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-erc20-token-account-balance-for-token-contract-address.md) for the provider-specific parameters and requirements.

