# Bridge: Get Transaction

Retrieves a transaction from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-transaction?connectionId=$CONNECTION_ID&userAccessToken=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userAccessToken": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-transaction?${params}`, {
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
| `userAccessToken` | string | yes | Bridge user access token returned by the Authorization token action. |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "amount": 1,
      "bookingDate": "2026-05-07T12:00:00.000Z",
      "bridgePaymentInformation": {
        "paymentLinkId": "https://example.com",
        "paymentRequestId": "string",
        "paymentTransactionId": "string"
      },
      "categoryId": 1,
      "cleanDescription": "string",
      "currencyCode": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "future": true,
      "id": 1,
      "operationType": "string",
      "providerDescription": "string",
      "transactionDate": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "valueDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Transaction's account unique identifier |
| `amount` | number | Transaction's amount A positive value indicates a credit and a negative value indicates a debit |
| `bookingDate` | date | Actual date when the transaction is posted to the account |
| `bridgePaymentInformation` | object | The information of bridge payment entities after successful reconciliation |
| `bridgePaymentInformation.paymentLinkId` | string | The id of the payment link the transaction was reconciled with |
| `bridgePaymentInformation.paymentRequestId` | string | The id of the payment request the transaction was reconciled with |
| `bridgePaymentInformation.paymentTransactionId` | string | The id of the payment transaction the transaction was reconciled with |
| `categoryId` | number | Transaction's category unique identifier |
| `cleanDescription` | string | Transaction's description cleaned and processed by the API |
| `currencyCode` | string | 3 letters ISO 4217 currency code |
| `date` | date | Transaction date |
| `deleted` | boolean | Flag to indicate that the transaction was deleted |
| `future` | boolean | Flag to indicate that the transaction will be debited in the future and doesn’t affect the account’s balance |
| `id` | number | Transaction's unique identifier |
| `operationType` | string | Type the transactions as standard banking operation |
| `providerDescription` | string | Transaction's raw description taken from the provider |
| `transactionDate` | date | Date on which the banking transaction is carried out but the the balance is not affected |
| `updatedAt` | date | Timestamp recording when the transaction was last updated |
| `valueDate` | date | Value date of the transaction on the account |

## Native endpoint

Through the native Bridge API, this operation is `GET /aggregation/transactions/:id` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

