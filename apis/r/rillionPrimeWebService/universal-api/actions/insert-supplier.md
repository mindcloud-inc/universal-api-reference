# Rillion Prime Web Service: Insert Supplier

Insert a supplier into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplier": {},
  "supplier.supplier": "string",
  "supplier.supplierBankAccount[].bankAccount": "string",
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-supplier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplier": {},
    "supplier.supplier": "string",
    "supplier.supplierBankAccount[].bankAccount": "string",
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `supplier` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Supplier section. |
| `supplier.supplier` | string | yes | Supplier number in ERP system |
| `supplier.supplierBankAccount[]` | array<object> | no | Supplier Bank Account lines. |
| `supplier.supplierBankAccount[].bankAccount` | string | yes | Account number |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `supplier.company` | list<string> | no | Company |
| `supplier.name` | string | no | Name of the Bank or other description |
| `supplier.type` | number | no | Supplier type: 0=External; 1=Internal; 2=Temporary |
| `supplier.vatNo` | string | no | VAT registration number |
| `supplier.ean` | string | no | EAN code |
| `supplier.iban` | string | no | IBAN |
| `supplier.graceDays` | string | no | Grace days before payment, this value is translated to a payment term in Palette |
| `supplier.paymentTerm` | string | no | Payment term. The Payment term can also be set by using GraceDays |
| `supplier.blocked` | number | no | Block invoices from the supplier: 0=No; 1=Invoices cannot be transferred from invoice log; 2=Blocked for payment |
| `supplier.classified` | number | no | Classify: 0=No; 1=Yes |
| `supplier.isPerson` | number | no | Is person: 0=No; 1=Yes |
| `supplier.validTo` | date | no | A valid to date for a supplier |
| `supplier.cashDiscount` | number | no | Apply the supplier cash discount: 0=No; 1=Yes |
| `supplier.currency` | string | no | Default currency for supplier |
| `supplier.debtAccount` | string | no | Trade creditors account |
| `supplier.costAccount` | string | no | Default expenditure account |
| `supplier.vatCode` | string | no | VAT codes |
| `supplier.vatType` | string | no | VatType |
| `supplier.flowProposal` | string | no | Default flowproposal for the supplier |
| `supplier.object1` | string | no | Object of Type 1 linked to the supplier |
| `supplier.object2` | string | no | Object of Type 2 linked to the supplier |
| `supplier.object3` | string | no | Object of Type 3 linked to the supplier |
| `supplier.object4` | string | no | Object of Type 4 linked to the supplier |
| `supplier.object5` | string | no | Object of Type 5 linked to the supplier |
| `supplier.object6` | string | no | Object of Type 6 linked to the supplier |
| `supplier.object7` | string | no | Object of Type 7 linked to the supplier |
| `supplier.object8` | string | no | Object of Type 8 linked to the supplier |
| `supplier.address1` | string | no | Address detail 1 |
| `supplier.address2` | string | no | Address detail 2 |
| `supplier.address3` | string | no | Address detail 3 |
| `supplier.address4` | string | no | Address detail 4 |
| `supplier.address5` | string | no | Address detail 5 |
| `supplier.address6` | string | no | Address detail 6 |
| `supplier.tele1` | string | no | Telephone detail 1 |
| `supplier.tele2` | string | no | Telephone detail 2 |
| `supplier.tele3` | string | no | Telephone detail 3 |
| `supplier.www` | string | no | Internet address |
| `supplier.contact` | string | no | Contact person |
| `supplier.email` | string | no | E-mail to contact person |
| `supplier.purchaseOrderEmail` | string | no | E-mail to contact person for purchaseorder |
| `supplier.corporateIdentityNo` | string | no | Corporate Identity Number |
| `supplier.note` | string | no | Notes on supplier |
| `supplier.languageID` | string | no | Preferred language |
| `supplier.group1` | string | no | Free group 1 |
| `supplier.group2` | string | no | Free group 2 |
| `supplier.group3` | string | no | Free group 3 |
| `supplier.remove` | number | no | Should record be removed: 0=No; 1=Yes |
| `supplier.keyType` | number | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `supplier.checkPayReference` | number | no | Check for payment reference: 0=No checking; 1=Rule for global standard; 2=Rule for Finnish standard (GIK); 3=Rule for Swedish standard (OCR); 4=Rule for European standard (RF); 5=Rule for Danish standard (FIK); 6=Rule fo |
| `supplier.supplierBankAccount[].name` | string | no | Name of the Bank or other description |
| `supplier.supplierBankAccount[].default` | number | no | Is this Bank Account the default/preferred account number: 0=No; 1=Yes |
| `supplier.supplierBankAccount[].externalId` | string | no |  |
| `supplier.supplierBankAccount[].externalSource` | string | no |  |
| `supplier.externalId` | string | no |  |
| `supplier.externalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-supplier.md) for the provider-specific parameters and requirements.

