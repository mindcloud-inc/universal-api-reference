# Infura Ethereum: Estimate Gas

Retrieves a gas estimate from Infura Ethereum.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/estimate-gas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/estimate-gas?connectionId=$CONNECTION_ID&params%5B0%5D%5Bdata%5D=0x313ce567&params%5B0%5D%5Bto%5D=0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2&params%5B1%5D=latest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0][data]": "0x313ce567",
  "params[0][to]": "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
  "params[1]": "latest"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/estimate-gas?${params}`, {
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
| `params[0][data]` | string | yes | ABI-encoded function selector and arguments used for the estimate. Example: `0x313ce567`. |
| `params[0][to]` | string | yes | The target contract or recipient address for the gas estimate. Example: `0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2`. |
| `params[1]` | string | yes | The block number or canonical tag to estimate against. Example: `latest`. |

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
| `response` | string | The estimated gas amount as a hex quantity. |

## Native endpoint

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-gas.md) for the provider-specific parameters and requirements.

