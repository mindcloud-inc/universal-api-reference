# Poof: Fetch Gas Price

Retrieves current gas price data from Poof.

```
GET https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-gas-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-gas-price?connectionId=$CONNECTION_ID&crypto=usdc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crypto": "usdc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-gas-price?${params}`, {
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
| `crypto` | string | yes | Crypto asset code. Default: `usdc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gasFeeCurrency": "string",
      "gasFeeInUsd": "string",
      "gasFeeUsdc": "string",
      "gasPriceEth": "string",
      "gasUsed": "string",
      "transactionFee": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gasFeeCurrency` | string |  |
| `gasFeeInUsd` | string |  |
| `gasFeeUsdc` | string |  |
| `gasPriceEth` | string |  |
| `gasUsed` | string |  |
| `transactionFee` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST /gas_price` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-gas-price.md) for the provider-specific parameters and requirements.

