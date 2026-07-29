# Rillion Prime Web Service: List Invoices

List invoices from the Prime invoice queue.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices?connectionId=$CONNECTION_ID&updateQueueStatus=false" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "updateQueueStatus": "false"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices?${params}`, {
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
| `updateQueueStatus` | boolean | yes | When true, returned rows are marked as exported and leave the queue permanently. Keep false to read without consuming. Default: `false`. |
| `company` | list<string> | no | Company ID to scope the call. |
| `noOfRows` | string | no | Maximum number of rows to return. Leave empty for no limit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountCoding": [
        {}
      ],
      "accountCodingDate": "string",
      "amount": "string",
      "arrivalAccountCoded": "string",
      "asset": "string",
      "baseAmount": "string",
      "baseVatAmount": "string",
      "blocked": "string",
      "classified": "string",
      "company": "string",
      "contractMatch": "string",
      "credit": "string",
      "currency": "string",
      "debtAccount": "string",
      "discountGrossAmount": "string",
      "discountPercentage": "string",
      "dueDate": "string",
      "extraAmount": "string",
      "feeAmount1": "string",
      "feeAmount2": "string",
      "feeAmount3": "string",
      "invoiceDate": "string",
      "invoiceNo": "string",
      "invoiceSeries": "string",
      "paymentAmount": "string",
      "purchaseOrderMatch": "string",
      "status": "string",
      "supplier": "string",
      "supplierExternalId": "string",
      "supplierInvoiceNo": "string",
      "type": "string",
      "useDiscount": "string",
      "vatAmount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountCoding` | array<object> | Account coding lines. Line type: 0=trade creditors, 1=expense, 2=VAT. |
| `accountCodingDate` | string | Accounting date (yyyy-MM-dd). |
| `amount` | string | Amount in invoice currency. |
| `arrivalAccountCoded` | string |  |
| `asset` | string |  |
| `baseAmount` | string | Amount in accounting currency. |
| `baseVatAmount` | string |  |
| `blocked` | string | Blocked for payment. |
| `classified` | string |  |
| `company` | string | Company ID. |
| `contractMatch` | string |  |
| `credit` | string | Credit note flag. |
| `currency` | string | Invoice currency code. |
| `debtAccount` | string | Trade creditors account. |
| `discountGrossAmount` | string |  |
| `discountPercentage` | string |  |
| `dueDate` | string | Due date (yyyy-MM-dd). |
| `extraAmount` | string |  |
| `feeAmount1` | string |  |
| `feeAmount2` | string |  |
| `feeAmount3` | string |  |
| `invoiceDate` | string | Invoice date (yyyy-MM-dd). |
| `invoiceNo` | string | Invoice number. |
| `invoiceSeries` | string | Invoice series. |
| `paymentAmount` | string |  |
| `purchaseOrderMatch` | string | PO match status code 0-21. See Appendix A of the Prime Integration Tables. |
| `status` | string | Invoice status: 0=being processed/preliminary, 2=ready for deletion, 4=ready for definite recording, 5=update account coding on import, 6=updated coding on active invoice. |
| `supplier` | string | Supplier ID. |
| `supplierExternalId` | string | Supplier's external ID. |
| `supplierInvoiceNo` | string | Supplier's invoice number. |
| `type` | string | Invoice type: 0=External, 1=Internal, 2=Expense. |
| `useDiscount` | string |  |
| `vatAmount` | string | VAT amount in invoice currency. |

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

