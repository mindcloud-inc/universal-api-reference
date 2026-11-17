# NetSuite - Basic: Create Customer Payment

Creates a new customer payment in NetSuite.

```
POST https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/create-customer-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/create-customer-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/create-customer-payment', {
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
| `customer` | object | no |  |
| `customer.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `customer.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `payment` | number | no | Amount received from the customer. A zero payment can apply existing credits or deposits to invoices. |
| `tranDate` | date | no |  |
| `memo` | string | no |  |
| `autoApply` | boolean | no | Apply this payment to open receivables automatically. Existing credits and deposits must be selected separately. |
| `apply` | object | no | Apply this payment to specific invoices or other receivables. The structure is fixed: an `items` list containing one entry per transaction. Use the nested fields, or map the complete object. Each entry supports: - `doc.id`: the transaction's NetSuite internal ID; alternatively use `doc.externalId`. - `apply`: `true` to apply this payment. - `amount`: the amount to allocate to that transaction. - `line`: the target transaction's line ID, when needed. Single invoice — value for this Apply argument: ```json { "items": [ { "doc": { "id": "104" }, "apply": true, "amount": 200, "line": 0 } ] } ``` Multiple invoices — value for this Apply argument: ```json { "items": [ { "doc": { "id": "104" }, "apply": true, "amount": 125, "line": 0 }, { "doc": { "id": "205" }, "apply": true, "amount": 75, "line": 0 } ] } ``` Replace the example transaction IDs and line IDs with actual NetSuite values. Line ID 0 is an example, not a universal value. Amounts and the number of entries vary with the invoices being paid. Leave Auto Apply off when specifying allocations yourself. |
| `apply.items[]` | array<object> | no | One line per invoice or other receivable to pay. Add a line and set its Document, Apply, Payment, and Line ID fields. |
| `apply.items[].doc` | object | no | Invoice or other receivable being paid. Supply its internal ID or external ID. |
| `apply.items[].doc.id` | string | no | Internal ID of the invoice or other receivable to pay. Use this or External ID. |
| `apply.items[].doc.externalId` | string | no | External ID of the invoice or other receivable to pay. Use instead of ID. |
| `apply.items[].apply` | boolean | no | Set to true to apply this payment to the selected transaction. |
| `apply.items[].amount` | number | no | Amount of this payment to allocate to the selected transaction. |
| `apply.items[].line` | number | no | Target transaction line ID, when needed. Use the actual NetSuite line ID; 0 is only an example. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | object | no | Deposit account to use when the payment is not held in Undeposited Funds. |
| `account.id` | string | no | Deposit account to use when the payment is not held in Undeposited Funds. |
| `account.externalId` | string | no | Deposit account to use when the payment is not held in Undeposited Funds. |
| `arAcct` | object | no |  |
| `arAcct.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `arAcct.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `currency` | object | no |  |
| `currency.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `currency.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `exchangeRate` | number | no |  |
| `checkNumber` | string | no |  |
| `externalId` | string | no |  |
| `toBeEmailed` | boolean | no |  |
| `subsidiary` | object | no |  |
| `subsidiary.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `subsidiary.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `department` | object | no |  |
| `department.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `department.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `class` | object | no |  |
| `class.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `class.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `location` | object | no |  |
| `location.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `location.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `postingPeriod` | object | no |  |
| `postingPeriod.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `postingPeriod.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `customForm` | object | no |  |
| `customForm.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `customForm.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `nexus` | object | no |  |
| `nexus.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `nexus.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `paymentOption` | object | no |  |
| `paymentOption.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `paymentOption.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `paymentProcessingProfile` | object | no |  |
| `paymentProcessingProfile.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `paymentProcessingProfile.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `customerPaymentAuthorization` | object | no |  |
| `customerPaymentAuthorization.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `customerPaymentAuthorization.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `cardholderAuthentication` | object | no |  |
| `cardholderAuthentication.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `cardholderAuthentication.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `handlingMode` | object | no |  |
| `handlingMode.id` | list<string> | no | One of: `MIMIC`, `PROCESS`, `SAVE_ONLY`. |
| `paymentOperation` | object | no |  |
| `paymentOperation.id` | list<string> | no | One of: `CAPTURE`, `SALE`. |
| `undepFunds` | object | no |  |
| `undepFunds.id` | string | no | Identifier of the deposit destination option configured in NetSuite. |
| `cleared` | boolean | no |  |
| `clearedDate` | date | no |  |
| `excludeFromGLNumbering` | boolean | no |  |
| `dynamicDescriptor` | string | no |  |
| `inputReferenceCode` | string | no |  |
| `integrationId` | string | no |  |
| `originator` | string | no |  |
| `cardSwipe` | string | no |  |
| `debitKsn` | string | no |  |
| `debitPinBlock` | string | no |  |
| `paymentCardCsc` | string | no |  |
| `paymentDeviceId` | string | no |  |
| `paymentInstrumentLimit` | number | no |  |
| `tranId` | string | no |  |
| `credit` | object | no |  |
| `credit.items[]` | array<object> | no |  |
| `credit.items[].doc` | object | no |  |
| `credit.items[].doc.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `credit.items[].doc.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `credit.items[].apply` | boolean | no |  |
| `credit.items[].amount` | number | no |  |
| `credit.items[].line` | number | no |  |
| `deposit` | object | no |  |
| `deposit.items[]` | array<object> | no |  |
| `deposit.items[].doc` | object | no |  |
| `deposit.items[].doc.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `deposit.items[].doc.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `deposit.items[].apply` | boolean | no |  |
| `deposit.items[].amount` | number | no |  |
| `accountingBookDetail` | object | no |  |
| `accountingBookDetail.items[]` | array<object> | no |  |
| `accountingBookDetail.items[].accountingBook` | object | no |  |
| `accountingBookDetail.items[].accountingBook.id` | string | no | Internal ID of the referenced record. Supply this or its external ID. |
| `accountingBookDetail.items[].accountingBook.externalId` | string | no | External ID of the referenced record. Use instead of its internal ID. |
| `accountingBookDetail.items[].exchangeRate` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetSuite - Basic API returns.

## Native endpoint

Through the native NetSuite - Basic API, this operation is `POST /record/v1/customerPayment` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-payment.md) for the provider-specific parameters and requirements.

