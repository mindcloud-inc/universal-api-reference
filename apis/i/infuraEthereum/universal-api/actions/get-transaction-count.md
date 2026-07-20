# Infura Ethereum: Get Transaction Count

Retrieves an address transaction count from Infura Ethereum.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-count?connectionId=$CONNECTION_ID&params%5B0%5D=0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2&params%5B1%5D=latest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0]": "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
  "params[1]": "latest"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-transaction-count?${params}`, {
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
| `params[0]` | string | yes | The Ethereum account or contract address to inspect. Example: `0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2`. |
| `params[1]` | string | yes | The block number or canonical tag to query against. Example: `latest`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | The transaction count as a hex quantity. |

## Native endpoint

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-count.md) for the provider-specific parameters and requirements.

