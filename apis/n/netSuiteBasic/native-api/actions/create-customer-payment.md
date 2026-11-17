# Create Customer Payment with NetSuite - Basic

Creates a new customer payment in NetSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/record/v1/customerPayment`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [Create Customer Payment](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2026.1/index.html#/definitions/customerPayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | body | `object` | no | — |
| `customer.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `customer.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `payment` | body | `number` | no | Amount received from the customer. A zero payment can apply existing credits or deposits to invoices. |
| `tranDate` | body | `date` | no | — |
| `memo` | body | `string` | no | — |
| `autoApply` | body | `boolean` | no | Apply this payment to open receivables automatically. Existing credits and deposits must be selected separately. |
| `account` | body | `object` | no | Deposit account to use when the payment is not held in Undeposited Funds. |
| `account.id` | body | `string` | no | Deposit account to use when the payment is not held in Undeposited Funds. |
| `account.externalId` | body | `string` | no | Deposit account to use when the payment is not held in Undeposited Funds. |
| `arAcct` | body | `object` | no | — |
| `arAcct.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `arAcct.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `currency` | body | `object` | no | — |
| `currency.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `currency.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `exchangeRate` | body | `number` | no | — |
| `checkNumber` | body | `string` | no | — |
| `externalId` | body | `string` | no | — |
| `toBeEmailed` | body | `boolean` | no | — |
| `subsidiary` | body | `object` | no | — |
| `subsidiary.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `subsidiary.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `department` | body | `object` | no | — |
| `department.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `department.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `class` | body | `object` | no | — |
| `class.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `class.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `location` | body | `object` | no | — |
| `location.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `location.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `postingPeriod` | body | `object` | no | — |
| `postingPeriod.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `postingPeriod.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `customForm` | body | `object` | no | — |
| `customForm.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `customForm.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `nexus` | body | `object` | no | — |
| `nexus.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `nexus.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `paymentOption` | body | `object` | no | — |
| `paymentOption.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `paymentOption.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `paymentProcessingProfile` | body | `object` | no | — |
| `paymentProcessingProfile.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `paymentProcessingProfile.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `customerPaymentAuthorization` | body | `object` | no | — |
| `customerPaymentAuthorization.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `customerPaymentAuthorization.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `cardholderAuthentication` | body | `object` | no | — |
| `cardholderAuthentication.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `cardholderAuthentication.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `handlingMode` | body | `object` | no | — |
| `handlingMode.id` | body | `list<string>` | no | Accepted values: `MIMIC`, `PROCESS`, `SAVE_ONLY`. |
| `paymentOperation` | body | `object` | no | — |
| `paymentOperation.id` | body | `list<string>` | no | Accepted values: `CAPTURE`, `SALE`. |
| `undepFunds` | body | `object` | no | — |
| `undepFunds.id` | body | `string` | no | Identifier of the deposit destination option configured in NetSuite. |
| `cleared` | body | `boolean` | no | — |
| `clearedDate` | body | `date` | no | — |
| `excludeFromGLNumbering` | body | `boolean` | no | — |
| `dynamicDescriptor` | body | `string` | no | — |
| `inputReferenceCode` | body | `string` | no | — |
| `integrationId` | body | `string` | no | — |
| `originator` | body | `string` | no | — |
| `cardSwipe` | body | `string` | no | — |
| `debitKsn` | body | `string` | no | — |
| `debitPinBlock` | body | `string` | no | — |
| `paymentCardCsc` | body | `string` | no | — |
| `paymentDeviceId` | body | `string` | no | — |
| `paymentInstrumentLimit` | body | `number` | no | — |
| `tranId` | body | `string` | no | — |
| `apply` | body | `object` | no | Apply this payment to specific invoices or other receivables. The structure is fixed: an `items` list containing one entry per transaction. Use the nested fields, or map the complete object.  Each entry supports: - `doc.id`: the transaction's NetSuite internal ID; alternatively use `doc.externalId`. - `apply`: `true` to apply this payment. - `amount`: the amount to allocate to that transaction. - `line`: the target transaction's line ID, when needed.  Single invoice — value for this Apply argument: ```json {   "items": [     {       "doc": { "id": "104" },       "apply": true,       "amount": 200,       "line": 0     }   ] } ```  Multiple invoices — value for this Apply argument: ```json {   "items": [     { "doc": { "id": "104" }, "apply": true, "amount": 125, "line": 0 },     { "doc": { "id": "205" }, "apply": true, "amount": 75, "line": 0 }   ] } ```  Replace the example transaction IDs and line IDs with actual NetSuite values. Line ID 0 is an example, not a universal value. Amounts and the number of entries vary with the invoices being paid. Leave Auto Apply off when specifying allocations yourself. |
| `apply.items[]` | body | `array<object>` | no | One line per invoice or other receivable to pay. Add a line and set its Document, Apply, Payment, and Line ID fields. |
| `apply.items[].doc` | body | `object` | no | Invoice or other receivable being paid. Supply its internal ID or external ID. |
| `apply.items[].doc.id` | body | `string` | no | Internal ID of the invoice or other receivable to pay. Use this or External ID. |
| `apply.items[].doc.externalId` | body | `string` | no | External ID of the invoice or other receivable to pay. Use instead of ID. |
| `apply.items[].apply` | body | `boolean` | no | Set to true to apply this payment to the selected transaction. |
| `apply.items[].amount` | body | `number` | no | Amount of this payment to allocate to the selected transaction. |
| `apply.items[].line` | body | `number` | no | Target transaction line ID, when needed. Use the actual NetSuite line ID; 0 is only an example. |
| `credit` | body | `object` | no | — |
| `credit.items[]` | body | `array<object>` | no | — |
| `credit.items[].doc` | body | `object` | no | — |
| `credit.items[].doc.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `credit.items[].doc.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `credit.items[].apply` | body | `boolean` | no | — |
| `credit.items[].amount` | body | `number` | no | — |
| `credit.items[].line` | body | `number` | no | — |
| `deposit` | body | `object` | no | — |
| `deposit.items[]` | body | `array<object>` | no | — |
| `deposit.items[].doc` | body | `object` | no | — |
| `deposit.items[].doc.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `deposit.items[].doc.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `deposit.items[].apply` | body | `boolean` | no | — |
| `deposit.items[].amount` | body | `number` | no | — |
| `accountingBookDetail` | body | `object` | no | — |
| `accountingBookDetail.items[]` | body | `array<object>` | no | — |
| `accountingBookDetail.items[].accountingBook` | body | `object` | no | — |
| `accountingBookDetail.items[].accountingBook.id` | body | `string` | no | Internal ID of the referenced record. Supply this or its external ID. |
| `accountingBookDetail.items[].accountingBook.externalId` | body | `string` | no | External ID of the referenced record. Use instead of its internal ID. |
| `accountingBookDetail.items[].exchangeRate` | body | `number` | no | — |
