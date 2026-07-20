# Fatture in Cloud: Create Received Document

Creates a new received document in Fatture in Cloud.

```
POST https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-received-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-received-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-received-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | The ID of the company. |
| `data` | object | yes | The received document payload inside the provider data envelope. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amortization": 1,
      "amountGross": 1,
      "amountNet": 1,
      "amountOtherWithholdingTax": 1,
      "amountVat": 1,
      "amountWithholdingTax": 1,
      "attachmentUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": {
        "exchangeRate": "string",
        "id": "string",
        "symbol": "string"
      },
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "eInvoice": true,
      "entity": {
        "id": 1,
        "name": "Ava Chen"
      },
      "id": 1,
      "invoiceNumber": "string",
      "isDetailed": true,
      "isMarked": true,
      "nextDueDate": "2026-05-07T12:00:00.000Z",
      "paymentsList": [
        {
          "amount": 1,
          "dueDate": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "paidDate": "2026-05-07T12:00:00.000Z",
          "paymentAccount": {
            "id": 1,
            "name": "Ava Chen",
            "virtual": true
          },
          "paymentTerms": {
            "days": 1,
            "type": "string"
          },
          "status": "string"
        }
      ],
      "rcCenter": "string",
      "taxDeductibility": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vatDeductibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amortization` | number |  |
| `amountGross` | number |  |
| `amountNet` | number |  |
| `amountOtherWithholdingTax` | number |  |
| `amountVat` | number |  |
| `amountWithholdingTax` | number |  |
| `attachmentUrl` | string |  |
| `createdAt` | date |  |
| `currency.exchangeRate` | string |  |
| `currency.id` | string |  |
| `currency.symbol` | string |  |
| `date` | date |  |
| `description` | string |  |
| `eInvoice` | boolean |  |
| `entity.id` | number |  |
| `entity.name` | string |  |
| `id` | number |  |
| `invoiceNumber` | string |  |
| `isDetailed` | boolean |  |
| `isMarked` | boolean |  |
| `nextDueDate` | date |  |
| `paymentsList[].amount` | number |  |
| `paymentsList[].dueDate` | date |  |
| `paymentsList[].id` | number |  |
| `paymentsList[].paidDate` | date |  |
| `paymentsList[].paymentAccount.id` | number |  |
| `paymentsList[].paymentAccount.name` | string |  |
| `paymentsList[].paymentAccount.virtual` | boolean |  |
| `paymentsList[].paymentTerms.days` | number |  |
| `paymentsList[].paymentTerms.type` | string |  |
| `paymentsList[].status` | string |  |
| `rcCenter` | string |  |
| `taxDeductibility` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `vatDeductibility` | number |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `POST /c/:company_id/received_documents` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-received-document.md) for the provider-specific parameters and requirements.

