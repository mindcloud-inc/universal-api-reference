# Streamtime: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=1601169" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "1601169"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | number | yes | Invoice ID. Example: `1601169`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDatetime": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "currencyCode": "string",
      "discount": 1,
      "dueDate": "string",
      "exchangeRate": 1,
      "externalAccountingPlatformId": 1,
      "externalInvoiceId": "string",
      "id": 1,
      "instalment": 1,
      "invoiceCurrencyAmountPaidIncTax": 1,
      "invoiceCurrencyBalance": 1,
      "invoiceCurrencyTotalAmountExTax": 1,
      "invoiceCurrencyTotalAmountIncTax": 1,
      "invoiceCurrencyTotalAmountTax": 1,
      "invoiceDate": "string",
      "invoiceStatus": {},
      "invoiceType": {},
      "jobId": 1,
      "name": "Ava Chen",
      "number": "string",
      "paidDate": "string",
      "reference": "string",
      "sentByUserId": 1,
      "sentDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDatetime` | date | Created timestamp |
| `createdUserId` | number | Creator user ID |
| `currencyCode` | string | Currency code |
| `discount` | number | Discount percentage |
| `dueDate` | string | Due date |
| `exchangeRate` | number | Exchange rate |
| `externalAccountingPlatformId` | number | External accounting platform ID |
| `externalInvoiceId` | string | External invoice ID |
| `id` | number | Invoice ID |
| `instalment` | number | Instalment percentage |
| `invoiceCurrencyAmountPaidIncTax` | number | Paid amount including tax |
| `invoiceCurrencyBalance` | number | Outstanding balance |
| `invoiceCurrencyTotalAmountExTax` | number | Total amount excluding tax |
| `invoiceCurrencyTotalAmountIncTax` | number | Total amount including tax |
| `invoiceCurrencyTotalAmountTax` | number | Tax amount |
| `invoiceDate` | string | Invoice date |
| `invoiceStatus` | object | Invoice status |
| `invoiceType` | object | Invoice type |
| `jobId` | number | Job ID |
| `name` | string | Invoice name |
| `number` | string | Invoice number |
| `paidDate` | string | Paid date |
| `reference` | string | Invoice reference |
| `sentByUserId` | number | Sender user ID |
| `sentDate` | string | Invoice sent date |

## Native endpoint

Through the native Streamtime API, this operation is `GET /invoices/:invoice_id` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

