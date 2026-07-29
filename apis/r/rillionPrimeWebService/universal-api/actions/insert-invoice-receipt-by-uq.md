# Rillion Prime Web Service: Insert Invoice Receipt by UQ

Insert an invoice receipt identified by its unique key (company, supplier, supplier invoice number).

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-invoice-receipt-by-uq
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-invoice-receipt-by-uq" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceReceipt": {},
  "invoiceReceipt.invoiceSeries": "string",
  "invoiceReceipt.invoiceNo": 1,
  "invoiceReceipt.status": 1,
  "invoiceReceipt.queueStatus": 1,
  "company": "string",
  "supplier": "string",
  "supplierInvoiceNo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-invoice-receipt-by-uq', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceReceipt": {},
    "invoiceReceipt.invoiceSeries": "string",
    "invoiceReceipt.invoiceNo": 1,
    "invoiceReceipt.status": 1,
    "invoiceReceipt.queueStatus": 1,
    "company": "string",
    "supplier": "string",
    "supplierInvoiceNo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceReceipt` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, InvoiceReceipt section. |
| `invoiceReceipt.invoiceSeries` | string | yes | Invoice series |
| `invoiceReceipt.invoiceNo` | number | yes | Invoice number |
| `invoiceReceipt.status` | number | yes | The same status as the invoice had when it was exported from Prime |
| `invoiceReceipt.queueStatus` | number | yes | Queue status: 1=Correct; 2=Error |
| `company` | list<string> | yes | Company ID of the invoice. |
| `supplier` | string | yes | Supplier ID of the invoice. |
| `supplierInvoiceNo` | string | yes | Supplier invoice number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceReceipt.arrivalAccountCodingDate` | date | no | Accounting date for preliminary recording in ERP |
| `invoiceReceipt.voucherSeries` | string | no | Voucher series in ERP |
| `invoiceReceipt.voucherNo` | number | no | Voucher number in ERP |
| `invoiceReceipt.errorText` | string | no | Error text if QueueStatus=2 |
| `invoiceReceipt.invoiceExternalId` | string | no |  |
| `invoiceReceipt.invoiceExternalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-invoice-receipt-by-uq.md) for the provider-specific parameters and requirements.

