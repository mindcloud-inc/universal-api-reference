# Create Payment with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Payment`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create Payment](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CustomerID` | body | `object` | no |
| `CustomerID.value` | body | `string` | yes |
| `CashAccount` | body | `object` | no |
| `CashAccount.value` | body | `string` | yes |
| `PaymentAmount` | body | `object` | no |
| `PaymentAmount.value` | body | `number` | yes |
| `PaymentMethod` | body | `object` | no |
| `PaymentMethod.value` | body | `string` | yes |
| `Hold` | body | `object` | no |
| `Hold.value` | body | `boolean` | no |
| `Description` | body | `object` | no |
| `Description.value` | body | `string` | no |
| `Branch` | body | `object` | no |
| `Branch.value` | body | `string` | no |
| `CurrencyID` | body | `object` | no |
| `CurrencyID.value` | body | `string` | no |
| `DocumentsToApply[]` | body | `array<object>` | no |
| `DocumentsToApply[].DocType` | body | `object` | no |
| `DocumentsToApply[].DocType.value` | body | `string` | no |
| `DocumentsToApply[].DocLineNbr` | body | `object` | no |
| `DocumentsToApply[].DocLineNbr.value` | body | `string` | no |
| `DocumentsToApply[].ReferenceNbr` | body | `object` | no |
| `DocumentsToApply[].ReferenceNbr.value` | body | `string` | no |
| `OrdersToApply[]` | body | `array<object>` | no |
| `OrdersToApply[].OrderType` | body | `object` | no |
| `OrdersToApply[].OrderType.value` | body | `string` | no |
| `OrdersToApply[].OrderNbr` | body | `object` | no |
| `OrdersToApply[].OrderNbr.value` | body | `string` | no |
