# Avaza: Update Invoice

Updates an existing invoice in Avaza.

```
PUT https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldstoupdate": "string",
  "transactionid": 1,
  "lineitems": {},
  "lineitems[].inventoryitemidfk": 1,
  "lineitems[].quantity": 1,
  "lineitems[].unitprice": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldstoupdate": "string",
    "transactionid": 1,
    "lineitems": {},
    "lineitems[].inventoryitemidfk": 1,
    "lineitems[].quantity": 1,
    "lineitems[].unitprice": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldstoupdate` | list<string> | yes | Required: The collection of Field Names you wish to update. Possible Values: CustomerPONumber, DateIssued, PaymentTerms, DueDate, Subject, Notes, TransactionTaxConfigCode, ExchangeRate, InvoiceTemplateIDFK, InvoiceNumber, LineItems |
| `transactionid` | number | yes | The ID of the Invoice to update |
| `customerponumber` | string | no | Plain UTF8 text. 100 characters max |
| `dateissued` | date | no | The Date the Invoice is issued. Date should be specified as local date. |
| `paymentterms` | number | no |  |
| `duedate` | date | no | If the Due Date is specified then Payment Terms will be set to -1 (Custom). Otherwise DueDate will be auto calculated based on the provided IssueDate and Payment Term. Due Date must be greater than or equal to Issue Date. |
| `subject` | string | no | Invoice Subject in plain UTF8 text. (no HTML). 255 characters max |
| `notes` | string | no | Invoice Notes in plain UTF8 text. (no HTML). Max 2000 characters |
| `transactiontaxconfigcode` | string | no | Possible values are (EX --- Tax Exclusive, INC --- Tax Inclusive). If left set to null/emptystring it will use the account default. |
| `exchangerate` | number | no | Exchange rate is only valid for invoices in currency other than default account currency. If not specified it will get the market rate based on the Date Issued. |
| `invoicetemplateidfk` | number | no | And id for an invoice template in the account. If set to Null the account default invoice template will be used. |
| `invoicenumber` | string | no | Pass a string or integer. If an integer is passed then the largest integer will be use as the seed to auto generate the next invoice number in the sequence. |
| `lineitems` | list<object> | yes |  |
| `lineitems[].transactionlineitemid` | number | no | Optional ID of exisiting TransactionLineItem that should be retained and updated |
| `lineitems[].inventoryitemidfk` | number | yes | The ID of the InventoryItem this line item is linked to |
| `lineitems[].description` | string | no | Plain UTF8 text. (no HTML) |
| `lineitems[].quantity` | number | yes | The quantity for the line item |
| `lineitems[].unitprice` | number | yes | The unit price for the lineitem. |
| `lineitems[].taxidfk` | number | no | Must match an existing Tax ID. |
| `lineitems[].discount` | number | no | Enter 10.5 to give a 10.5% discount |
| `lineitems[].projectidfk` | number | no | Optional. Project ID of an Avaza Project that belongs to this customer, so line item is attributed to that Project for reporting. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `PUT /api/Invoice` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

