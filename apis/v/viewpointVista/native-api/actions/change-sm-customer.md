# Change SM Customer with Viewpoint Vista

Changes an existing SM Customer

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/change`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Change SM Customer](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomersactionschange)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `__key` | body | `object` | no | Key id(SMCustomerID). |
| `__key.KeyID` | body | `number` | yes | — |
| `Active` | body | `list<string>` | no | Optional. If omitted, `Y` will be defaulted. |
| `NonBillable` | body | `list<string>` | no | Optional.  If omitted, `N` will be defaulted. |
| `RateTemplate` | body | `string` | no | Key to SM Rate Template. Optional.   If omitted, null will be defaulted. |
| `BillToARCustomer` | body | `number` | no | Alternate Bill To Customer. Optional. Set the Alternate AR Customer to bill to for this SM Customer.  If omitted, null will be defaulted. |
| `CustomerPOSetting` | body | `list<string>` | no | Optional. If omitted, `N` will be defaulted.  Allowed: - `R` - Required - `N` - Not Required |
| `PrimaryTechnician` | body | `string` | no | Key to SM Technician. Optional.  If omitted, null will be defaulted. |
| `Reviewer` | body | `string` | no | Key to `hq/reviewers(Reviewer)`. Optional.  If omitted, null will be defaulted. |
| `InvoiceGrouping` | body | `list<string>` | no | Optional.  Allowed: - `C`-One per Customer, - `S`-One per service site - `W`-One per work order - `P`-One per work order scope.  If omitted, `C` will be defaulted. Maximum length: 1. |
| `InvoiceGroupingPOOverride` | body | `list<string>` | no | Optional. If omitted, `N` will be defaulted. |
| `InvoiceSummaryLevel` | body | `string` | no | Optional. If omitted, `T-Transaction` will be defaulted.  Options: - `L-Line Type` - `C-Cost Type` - `T-Transaction` |
| `ReportID` | body | `number` | no | — |
| `DeliveryTo` | body | `list<string>` | no | Invoice Delivery Address Type.  Options: - `A` AR Customer - `S` Service Site - `O` Other   `S` Service Site can only be provided if the `InvoiceGrouping` != `C` |
| `DeliveryMethod` | body | `list<string>` | no | If omitted, `P` will be defaulted. |
| `billingEmail` | body | `string` | no | If omitted, null will be defaulted.  Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingName` | body | `string` | no | If omitted, null will be defaulted.  Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingAddress1` | body | `string` | no | If omitted, null will be defaulted.  Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingAddress2` | body | `string` | no | If omitted, null will be defaulted.  Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingCity` | body | `string` | no | If omitted, null will be defaulted.  Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingState` | body | `string` | no | If omitted, null will be defaulted.  Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingPostalCode` | body | `string` | no | If omitted, null will be defaulted.  Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingCountry` | body | `string` | no | If omitted, null will be defaulted.  Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `Notes` | body | `string` | no | — |
