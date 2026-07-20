# Escrow.com: Get Transaction Disbursement Methods

Retrieves transaction disbursement methods from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-disbursement-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-disbursement-methods?connectionId=$CONNECTION_ID&transactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-disbursement-methods?${params}`, {
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
| `transactionId` | number | yes | The Escrow.com transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableDisbursementMethods": [
        {}
      ],
      "savedDisbursementMethods": [
        {}
      ],
      "selectedDisbursementMethod": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableDisbursementMethods` | array<object> | Available disbursement methods for the transaction. |
| `savedDisbursementMethods` | array<object> | Saved disbursement method profiles available to use. |
| `selectedDisbursementMethod` | object | Selected disbursement method when one has been chosen. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /transaction/:transaction_id/disbursement_methods` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-disbursement-methods.md) for the provider-specific parameters and requirements.

