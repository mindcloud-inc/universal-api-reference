# Visma eAccounting: Create Customer Invoice Payment

Creates a customer invoice payment in Visma eAccounting.

```
POST https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-customer-invoice-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-customer-invoice-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-customer-invoice-payment', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "bankTransactionId": "string",
      "companyBankAccountId": "string",
      "paymentAmount": 1,
      "paymentCurrency": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bankTransactionId` | string |  |
| `companyBankAccountId` | string |  |
| `paymentAmount` | number |  |
| `paymentCurrency` | string |  |
| `paymentDate` | date |  |
| `reference` | string |  |

## Native endpoint

Through the native Visma eAccounting API, this operation is `POST /customerinvoices/{invoiceId}/payments` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-invoice-payment.md) for the provider-specific parameters and requirements.

