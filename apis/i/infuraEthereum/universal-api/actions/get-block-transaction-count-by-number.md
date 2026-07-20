# Infura Ethereum: Get Block Transaction Count By Number

Retrieves block transaction count from Infura Ethereum by number.

```
GET https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-transaction-count-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infura Ethereum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-transaction-count-by-number?connectionId=$CONNECTION_ID&params%5B0%5D=latest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params[0]": "latest"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-block-transaction-count-by-number?${params}`, {
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
| `params[0]` | string | yes | The block number or canonical tag to query against. Example: `latest`. |

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
| `response` | string | The number of transactions in the block as a hex quantity. |

## Native endpoint

Through the native Infura Ethereum API, this operation is `POST /v3/:apiKey` (base URL `https://mainnet.infura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-transaction-count-by-number.md) for the provider-specific parameters and requirements.

