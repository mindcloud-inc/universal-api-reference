# Invoice Ninja: Refund Payment



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/refund-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/refund-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "amount": 1,
  "date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/refund-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "amount": 1,
    "date": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The payment to refund. |
| `amount` | number | yes | Refund amount. |
| `date` | string | yes | Refund date. |
| `privateNotes` | string | no | Internal refund notes. |
| `invoices` | list<object> | no | Invoices receiving the refund allocation. |
| `transactionReference` | string | no | Refund transaction reference. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "applied": 1,
      "archivedAt": 1,
      "clientId": "string",
      "createdAt": 1,
      "currencyId": "string",
      "date": "string",
      "documents": [
        {}
      ],
      "exchangeRate": 1,
      "id": "string",
      "isDeleted": true,
      "isManual": true,
      "number": "string",
      "paymentables": [
        {}
      ],
      "privateNotes": "string",
      "refunded": 1,
      "statusId": "string",
      "transactionReference": "string",
      "typeId": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `applied` | number |  |
| `archivedAt` | number |  |
| `clientId` | string |  |
| `createdAt` | number |  |
| `currencyId` | string |  |
| `date` | string |  |
| `documents` | array<object> |  |
| `exchangeRate` | number |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isManual` | boolean |  |
| `number` | string |  |
| `paymentables` | array<object> |  |
| `privateNotes` | string |  |
| `refunded` | number |  |
| `statusId` | string |  |
| `transactionReference` | string |  |
| `typeId` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `POST /payments/refund` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-payment.md) for the provider-specific parameters and requirements.

