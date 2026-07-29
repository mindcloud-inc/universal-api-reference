# Rillion Prime Web Service: Insert Invoice

Insert an invoice into the Prime invoice queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": {},
  "invoice.invoiceSeries": "string",
  "invoice.invoiceNo": 1,
  "invoice.company": "string",
  "invoice.credit": "string",
  "invoice.type": 1,
  "invoice.status": 1,
  "invoice.classified": "string",
  "invoice.blocked": "string",
  "invoice.supplier": "string",
  "invoice.supplierInvoiceNo": "string",
  "invoice.invoiceDate": "2026-05-07T12:00:00.000Z",
  "invoice.dueDate": "2026-05-07T12:00:00.000Z",
  "invoice.accountCodingDate": "2026-05-07T12:00:00.000Z",
  "invoice.currency": "string",
  "invoice.amount": 1,
  "invoice.baseAmount": 1,
  "invoice.vatAmount": 1,
  "invoice.baseVatAmount": 1,
  "invoice.feeAmount1": 1,
  "invoice.feeAmount2": 1,
  "invoice.feeAmount3": 1,
  "invoice.paymentAmount": 1,
  "invoice.debtAccount": "string",
  "invoice.account": "string",
  "invoice.vatCode": "string",
  "invoice.arrivalAccountCoded": "string",
  "invoice.asset": "string",
  "invoice.purchaseOrderMatch": 1,
  "invoice.accountCoding[].type": 1,
  "invoice.accountCoding[].account": "string",
  "invoice.accountCoding[].currency": "string",
  "invoice.accountCoding[].amount": 1,
  "invoice.accountCoding[].baseAmount": 1,
  "invoice.accountCoding[].lineVatAmount": 1,
  "invoice.accountCoding[].vatCode": "string",
  "invoice.accountCoding[].vatDeduction": 1,
  "invoice.accountCoding[].forwardInvoice": 1,
  "invoice.contractMatch": 1,
  "invoice.useDiscount": true,
  "invoice.discountGrossAmount": true,
  "invoice.discountPercentage": 1,
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": {},
    "invoice.invoiceSeries": "string",
    "invoice.invoiceNo": 1,
    "invoice.company": "string",
    "invoice.credit": "string",
    "invoice.type": 1,
    "invoice.status": 1,
    "invoice.classified": "string",
    "invoice.blocked": "string",
    "invoice.supplier": "string",
    "invoice.supplierInvoiceNo": "string",
    "invoice.invoiceDate": "2026-05-07T12:00:00.000Z",
    "invoice.dueDate": "2026-05-07T12:00:00.000Z",
    "invoice.accountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoice.currency": "string",
    "invoice.amount": 1,
    "invoice.baseAmount": 1,
    "invoice.vatAmount": 1,
    "invoice.baseVatAmount": 1,
    "invoice.feeAmount1": 1,
    "invoice.feeAmount2": 1,
    "invoice.feeAmount3": 1,
    "invoice.paymentAmount": 1,
    "invoice.debtAccount": "string",
    "invoice.account": "string",
    "invoice.vatCode": "string",
    "invoice.arrivalAccountCoded": "string",
    "invoice.asset": "string",
    "invoice.purchaseOrderMatch": 1,
    "invoice.accountCoding[].type": 1,
    "invoice.accountCoding[].account": "string",
    "invoice.accountCoding[].currency": "string",
    "invoice.accountCoding[].amount": 1,
    "invoice.accountCoding[].baseAmount": 1,
    "invoice.accountCoding[].lineVatAmount": 1,
    "invoice.accountCoding[].vatCode": "string",
    "invoice.accountCoding[].vatDeduction": 1,
    "invoice.accountCoding[].forwardInvoice": 1,
    "invoice.contractMatch": 1,
    "invoice.useDiscount": true,
    "invoice.discountGrossAmount": true,
    "invoice.discountPercentage": 1,
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoice` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Invoice section. |
| `invoice.invoiceSeries` | string | yes | Invoice series |
| `invoice.invoiceNo` | number | yes | Invoice number |
| `invoice.company` | list<string> | yes | Company |
| `invoice.credit` | string | yes | Credit note: 0=No; 1=Yes |
| `invoice.type` | number | yes | Invoice type: 0=External; 1=Internal; 2=Expense |
| `invoice.status` | number | yes | Invoice status: 0=Being processed/for preliminary recording; 2=Ready for deletion; 4=Ready for definite recording; 5=Update account coding on import; 6=Updated account coding on active invoice |
| `invoice.classified` | string | yes | Classified invoice: 0=No; 1=Yes |
| `invoice.blocked` | string | yes | Blocked for payment: 0=No; 1=Yes |
| `invoice.supplier` | string | yes | Supplier ID |
| `invoice.supplierInvoiceNo` | string | yes | Supplier’s invoice number |
| `invoice.invoiceDate` | date | yes | Invoice date |
| `invoice.dueDate` | date | yes | Due date |
| `invoice.accountCodingDate` | date | yes | Accounting date |
| `invoice.currency` | string | yes | Currency on posting line |
| `invoice.amount` | number | yes |  |
| `invoice.baseAmount` | number | yes | Amount in currency for accounting purposes |
| `invoice.vatAmount` | number | yes | VAT amount in the invoice’s currency |
| `invoice.baseVatAmount` | number | yes | VAT amount in currency for accounting purposes |
| `invoice.feeAmount1` | number | yes | Extra fee type 1 |
| `invoice.feeAmount2` | number | yes | Extra fee type 2 |
| `invoice.feeAmount3` | number | yes | Extra fee type 3 |
| `invoice.paymentAmount` | number | yes | Amount payable when QueueType=2 |
| `invoice.debtAccount` | string | yes | Trade creditors account |
| `invoice.account` | string | yes | Account |
| `invoice.vatCode` | string | yes | VAT code |
| `invoice.arrivalAccountCoded` | string | yes | Preliminary recorded: 0=No; 1=Yes |
| `invoice.asset` | string | yes | Refers to an asset record: 0=No; 1=Yes |
| `invoice.purchaseOrderMatch` | number | yes | See Appendix A for match status. |
| `invoice.accountCoding[]` | array<object> | no | Account Coding lines. |
| `invoice.accountCoding[].type` | number | yes | Type of posting line: 0=Trade creds; 1=Expenses line; 2=VAT line |
| `invoice.accountCoding[].account` | string | yes | Account |
| `invoice.accountCoding[].currency` | string | yes | Currency on posting line |
| `invoice.accountCoding[].amount` | number | yes |  |
| `invoice.accountCoding[].baseAmount` | number | yes | Amount in currency for accounting purposes |
| `invoice.accountCoding[].lineVatAmount` | number | yes | Calculated line VAT amount |
| `invoice.accountCoding[].vatCode` | string | yes | VAT code |
| `invoice.accountCoding[].vatDeduction` | number | yes |  |
| `invoice.accountCoding[].forwardInvoice` | number | yes | Reinvoice: 0=No; 1=For reinvoicing; 2=Reinvoiced |
| `invoice.contractMatch` | number | yes | Invoice matched to a Contract: 0=Not matched to a Contract; 1=Partly matched to a Contract; 2=Fully matched to a Contract |
| `invoice.useDiscount` | boolean | yes | Make use or the cash discount: 0=No; 1=Yes |
| `invoice.discountGrossAmount` | boolean | yes | DiscountAmount calculation based on Gross Amount 0=No; 1=Yes |
| `invoice.discountPercentage` | number | yes | Discount percentage used in calculation of DiscountAmount |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoice.purchaseOrderNo` | string | no | Order number |
| `invoice.contractNo` | string | no | Contract number |
| `invoice.authorizationUser` | string | no | Signed by user |
| `invoice.authorizationRole` | string | no | Signed by role |
| `invoice.object1` | string | no | Object of Type 1 |
| `invoice.object2` | string | no | Object of Type 2 |
| `invoice.object3` | string | no | Object of Type 3 |
| `invoice.object4` | string | no | Object of Type 4 |
| `invoice.object5` | string | no | Object of Type 5 |
| `invoice.object6` | string | no | Object of Type 6 |
| `invoice.object7` | string | no | Object of Type 7 |
| `invoice.object8` | string | no | Object of Type 8 |
| `invoice.arrivalAccountCodingDate` | date | no | Preliminary recording date |
| `invoice.voucherSeries` | string | no | Voucher series |
| `invoice.voucherNo` | number | no | Voucher number |
| `invoice.paymentDate` | date | no | Date for final payment of the invoice |
| `invoice.alternativeID` | string | no | Alternative ID |
| `invoice.linkedInvoiceSeries` | string | no | Invoice series of invoice that invoice is linked to, e.g. credit note |
| `invoice.linkedInvoiceNo` | number | no | Invoice number of invoice that invoice is linked to, e.g. credit note |
| `invoice.payReference` | string | no | Payment reference number, e.g. OCR/IBAN/KID |
| `invoice.deliveryNote` | string | no | GRN refering to the invoice |
| `invoice.extraID` | string | no | Extra identification field |
| `invoice.extraAmount` | number | no | Extra amount field |
| `invoice.purchaseOrderMatchType` | number | no |  |
| `invoice.reference1` | string | no | Invoice reference 1 |
| `invoice.reference2` | string | no | Invoice reference 2 |
| `invoice.note` | string | no | Free text |
| `invoice.group1` | string | no | Free group 1 |
| `invoice.group2` | string | no | Free group 2 |
| `invoice.group3` | string | no | Free group 3 |
| `invoice.group4` | string | no | Free group 4 |
| `invoice.group5` | string | no | Free group 5 |
| `invoice.group6` | string | no | Free group 6 |
| `invoice.paymentMessage` | string | no | Payment message |
| `invoice.accountCoding[].createUser` | string | no | Created by user |
| `invoice.accountCoding[].createRole` | string | no | Created by role |
| `invoice.accountCoding[].acceptUser` | string | no | Acceptance user from external ERP |
| `invoice.accountCoding[].acceptRole` | string | no | Acceptance role from external ERP |
| `invoice.accountCoding[].signUser` | string | no | Signed by user |
| `invoice.accountCoding[].signRole` | string | no | Signed by role |
| `invoice.accountCoding[].object1` | string | no | Object of Type 1 |
| `invoice.accountCoding[].object2` | string | no | Object of Type 2 |
| `invoice.accountCoding[].object3` | string | no | Object of Type 3 |
| `invoice.accountCoding[].object4` | string | no | Object of Type 4 |
| `invoice.accountCoding[].object5` | string | no | Object of Type 5 |
| `invoice.accountCoding[].object6` | string | no | Object of Type 6 |
| `invoice.accountCoding[].object7` | string | no | Object of Type 7 |
| `invoice.accountCoding[].object8` | string | no | Object of Type 8 |
| `invoice.accountCoding[].invoiceAccountCodingLineNo` | number | no | Line number |
| `invoice.accountCoding[].number` | number | no | Quantity |
| `invoice.accountCoding[].allocationType` | string | no | Allocation type |
| `invoice.accountCoding[].allocationsAccount` | string | no | Allocations account |
| `invoice.accountCoding[].allocateFromDate` | date | no | Allocate from |
| `invoice.accountCoding[].allocateToDate` | date | no | Allocate until |
| `invoice.accountCoding[].assetType` | string | no | Asset type |
| `invoice.accountCoding[].assetName` | string | no | Asset name |
| `invoice.accountCoding[].assetDescription` | string | no | Asset description |
| `invoice.accountCoding[].assetDate` | date | no | Purchase date for asset |
| `invoice.accountCoding[].ownerAsset` | string | no | Belongs to existing asset |
| `invoice.accountCoding[].purchaseOrderNo` | string | no | Order number |
| `invoice.accountCoding[].purchaseOrderLineNo` | string | no | Order line ID |
| `invoice.accountCoding[].note` | string | no | Free text |
| `invoice.accountCoding[].group1` | string | no | Free group 1 |
| `invoice.accountCoding[].group2` | string | no | Free group 2 |
| `invoice.accountCoding[].group3` | string | no | Free group 3 |
| `invoice.accountCoding[].group4` | string | no | Free group 4 |
| `invoice.accountCoding[].group5` | string | no | Free group 5 |
| `invoice.accountCoding[].group6` | string | no | Free group 6 |
| `invoice.accountCoding[].purchaseOrderItem` | string | no |  |
| `invoice.accountCoding[].currencyExternalId` | string | no |  |
| `invoice.accountCoding[].currencyExternalSource` | string | no |  |
| `invoice.accountCoding[].purchaseOrderExternalId` | string | no |  |
| `invoice.accountCoding[].purchaseOrderExternalSource` | string | no |  |
| `invoice.accountCoding[].vatCodeExternalId` | string | no |  |
| `invoice.accountCoding[].vatCodeExternalSource` | string | no |  |
| `invoice.accountCoding[].accountExternalId` | string | no |  |
| `invoice.accountCoding[].accountExternalSource` | string | no |  |
| `invoice.accountCoding[].assetExternalId` | string | no |  |
| `invoice.accountCoding[].assetExternalSource` | string | no |  |
| `invoice.accountCoding[].object1ExternalId` | string | no |  |
| `invoice.accountCoding[].object1ExternalSource` | string | no |  |
| `invoice.accountCoding[].object2ExternalId` | string | no |  |
| `invoice.accountCoding[].object2ExternalSource` | string | no |  |
| `invoice.accountCoding[].object3ExternalId` | string | no |  |
| `invoice.accountCoding[].object3ExternalSource` | string | no |  |
| `invoice.accountCoding[].object4ExternalId` | string | no |  |
| `invoice.accountCoding[].object4ExternalSource` | string | no |  |
| `invoice.accountCoding[].object5ExternalId` | string | no |  |
| `invoice.accountCoding[].object5ExternalSource` | string | no |  |
| `invoice.accountCoding[].object6ExternalId` | string | no |  |
| `invoice.accountCoding[].object6ExternalSource` | string | no |  |
| `invoice.accountCoding[].object7ExternalId` | string | no |  |
| `invoice.accountCoding[].object7ExternalSource` | string | no |  |
| `invoice.accountCoding[].object8ExternalId` | string | no |  |
| `invoice.accountCoding[].object8ExternalSource` | string | no |  |
| `invoice.supplierBankAccount` | string | no | Bankaccount for payment |
| `invoice.discountDate` | date | no | Payment date to make use of the cash discount |
| `invoice.discountAmount` | number | no | Payment amount if make use of the cash discount |
| `invoice.externalId` | string | no |  |
| `invoice.externalSource` | string | no |  |
| `invoice.linkedInvoiceExternalId` | string | no |  |
| `invoice.linkedInvoiceExternalSource` | string | no |  |
| `invoice.supplierExternalId` | string | no |  |
| `invoice.supplierExternalSource` | string | no |  |
| `invoice.purchaseOrderExternalId` | string | no |  |
| `invoice.purchaseOrderExternalSource` | string | no |  |
| `invoice.vatCodeExternalId` | string | no |  |
| `invoice.vatCodeExternalSource` | string | no |  |
| `invoice.currencyExternalId` | string | no |  |
| `invoice.currencyExternalSource` | string | no |  |
| `invoice.accountExternalId` | string | no |  |
| `invoice.accountExternalSource` | string | no |  |
| `invoice.supplierBankAccountExternalId` | string | no |  |
| `invoice.supplierBankAccountExternalSource` | string | no |  |
| `invoice.object1ExternalId` | string | no |  |
| `invoice.object1ExternalSource` | string | no |  |
| `invoice.objectType1ExternalId` | string | no |  |
| `invoice.objectType1ExternalSource` | string | no |  |
| `invoice.object2ExternalId` | string | no |  |
| `invoice.object2ExternalSource` | string | no |  |
| `invoice.objectType2ExternalId` | string | no |  |
| `invoice.objectType2ExternalSource` | string | no |  |
| `invoice.object3ExternalId` | string | no |  |
| `invoice.object3ExternalSource` | string | no |  |
| `invoice.objectType3ExternalId` | string | no |  |
| `invoice.objectType3ExternalSource` | string | no |  |
| `invoice.object4ExternalId` | string | no |  |
| `invoice.object4ExternalSource` | string | no |  |
| `invoice.objectType4ExternalId` | string | no |  |
| `invoice.objectType4ExternalSource` | string | no |  |
| `invoice.object5ExternalId` | string | no |  |
| `invoice.object5ExternalSource` | string | no |  |
| `invoice.objectType5ExternalId` | string | no |  |
| `invoice.objectType5ExternalSource` | string | no |  |
| `invoice.object6ExternalId` | string | no |  |
| `invoice.object6ExternalSource` | string | no |  |
| `invoice.objectType6ExternalId` | string | no |  |
| `invoice.objectType6ExternalSource` | string | no |  |
| `invoice.object7ExternalId` | string | no |  |
| `invoice.object7ExternalSource` | string | no |  |
| `invoice.objectType7ExternalId` | string | no |  |
| `invoice.objectType7ExternalSource` | string | no |  |
| `invoice.object8ExternalId` | string | no |  |
| `invoice.object8ExternalSource` | string | no |  |
| `invoice.objectType8ExternalId` | string | no |  |
| `invoice.objectType8ExternalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-invoice.md) for the provider-specific parameters and requirements.

