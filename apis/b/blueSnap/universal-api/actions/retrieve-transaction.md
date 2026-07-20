# BlueSnap: Retrieve Transaction

Retrieves a transaction from BlueSnap.

```
GET https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-transaction?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-transaction?${params}`, {
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
| `transactionId` | string | yes | BlueSnap transaction ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cardTransactionType": "string",
      "creditCard": {
        "cardLastFourDigits": "string",
        "cardType": "string"
      },
      "currency": "string",
      "processingInfo": {
        "processingStatus": "string"
      },
      "refunds": {
        "balanceAmount": 1,
        "refund": [
          {
            "amount": 1,
            "currency": "string",
            "date": "string",
            "refundTransactionId": 1
          }
        ]
      },
      "transactionApprovalDate": "string",
      "transactionApprovalTime": "string",
      "transactionId": "string",
      "usdAmount": 1,
      "vaultedShopperId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Transaction amount. |
| `cardTransactionType` | string | Card transaction type. |
| `creditCard.cardLastFourDigits` | string | Card last four digits. |
| `creditCard.cardType` | string | Card type. |
| `currency` | string | Currency. |
| `processingInfo.processingStatus` | string | Processing status. |
| `refunds.balanceAmount` | number | Remaining refundable balance. |
| `refunds.refund[].amount` | number | Refund amount. |
| `refunds.refund[].currency` | string | Refund currency. |
| `refunds.refund[].date` | string | Refund date. |
| `refunds.refund[].refundTransactionId` | number | Refund transaction ID. |
| `transactionApprovalDate` | string | Approval date. |
| `transactionApprovalTime` | string | Approval time. |
| `transactionId` | string | Transaction ID. |
| `usdAmount` | number | USD amount. |
| `vaultedShopperId` | number | Vaulted shopper ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `GET /transactions/:transactionId` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-transaction.md) for the provider-specific parameters and requirements.

