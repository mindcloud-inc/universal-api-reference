# Flow Blockchain: Get Transaction Result

Retrieves a transaction result from Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-transaction-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-transaction-result?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-transaction-result?${params}`, {
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
| `transactionId` | string | yes | Transaction ID whose result should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block_id": "string",
      "computation_used": "string",
      "error_message": "string",
      "events": [
        {}
      ],
      "status": "string",
      "status_code": 1,
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block_id` | string | Block ID containing the transaction result. |
| `computation_used` | string | Computation used by execution. |
| `error_message` | string | Execution error message when present. |
| `events` | array<object> | Events emitted by the transaction. |
| `status` | string | Transaction status. |
| `status_code` | number | Transaction status code. |
| `transaction_id` | string | Flow transaction ID. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /transaction_results/{transaction_id}` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-result.md) for the provider-specific parameters and requirements.

