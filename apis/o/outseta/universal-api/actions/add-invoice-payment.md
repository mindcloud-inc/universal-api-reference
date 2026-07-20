# Outseta: Add Invoice Payment

Creates an invoice payment in Outseta.

```
POST https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-invoice-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-invoice-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-invoice-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account.uid` | string | no |  |
| `invoice.uid` | string | no |  |
| `amount` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Amount": 1,
      "BillingTransactionType": 1,
      "Created": "string",
      "TransactionDate": "string",
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Amount` | number |  |
| `BillingTransactionType` | number |  |
| `Created` | string |  |
| `TransactionDate` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `POST /billing/transactions/payment` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-invoice-payment.md) for the provider-specific parameters and requirements.

