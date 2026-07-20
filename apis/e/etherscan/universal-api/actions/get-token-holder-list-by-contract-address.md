# Etherscan: Get Token Holder List by Contract Address

Retrieves the token holder list for a contract.

```
GET https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-token-holder-list-by-contract-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Etherscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-token-holder-list-by-contract-address?connectionId=$CONNECTION_ID&contractAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-token-holder-list-by-contract-address?${params}`, {
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
| `page` | number | no | Default: `1`. |
| `offset` | number | no | Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": [
        {}
      ],
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
| `result` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Etherscan API, this operation is `GET /v2/api` (base URL `https://api.etherscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-holder-list-by-contract-address.md) for the provider-specific parameters and requirements.

