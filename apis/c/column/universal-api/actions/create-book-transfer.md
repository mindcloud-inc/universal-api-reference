# Column: Create Book Transfer



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/create-book-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/create-book-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currencyCode": "USD"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/create-book-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currencyCode": "USD"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Amount in cents of the book transfer. |
| `currencyCode` | string | yes | ISO 4217 currency code for the transfer. Default: `USD`. |
| `senderBankAccountId` | string | no | Sender bank account ID. Provide either Sender Bank Account ID or Sender Account Number ID. |
| `receiverBankAccountId` | string | no | Receiver bank account ID. Provide either Receiver Bank Account ID or Receiver Account Number ID. |
| `description` | string | no | Description visible in account activity. |
| `hold` | boolean | no | Create the book transfer in hold state so it can be cleared or canceled later. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderAccountNumberId` | string | no | Specific sender account number ID. |
| `receiverAccountNumberId` | string | no | Specific receiver account number ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowOverdraft": true,
      "amount": 1,
      "createdAt": "string",
      "currencyCode": "string",
      "description": "string",
      "id": "string",
      "idempotencyKey": "string",
      "receiverAccountNumberId": "string",
      "receiverBankAccountId": "string",
      "senderAccountNumberId": "string",
      "senderBankAccountId": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowOverdraft` | boolean |  |
| `amount` | number |  |
| `createdAt` | string |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `id` | string |  |
| `idempotencyKey` | string |  |
| `receiverAccountNumberId` | string |  |
| `receiverBankAccountId` | string |  |
| `senderAccountNumberId` | string |  |
| `senderBankAccountId` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Column API, this operation is `POST /transfers/book` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-book-transfer.md) for the provider-specific parameters and requirements.

