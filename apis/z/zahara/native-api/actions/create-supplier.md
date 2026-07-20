# Create Supplier with Zahara

Creates a new supplier in Zahara.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/{businessUnitApiKey}/Supplier/Add`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Create Supplier](https://ask.zaharasoftware.com/api-docs/add-supplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Address` | body | `object` | yes | Supplier address object. |
| `ContactName` | body | `string` | yes | Primary supplier contact name. |
| `CountryCode` | body | `string` | yes | Supplier ISO country code. |
| `CountryCodeId` | body | `number` | yes | Supplier country code ID. |
| `DefaultNominalCode` | body | `string` | yes | Default nominal code. |
| `DefaultPaymentTerms` | body | `number` | yes | Default payment terms value. |
| `PaymentTermStartType` | body | `number` | yes | Payment term start type. |
| `PaymentTermDaysNumber` | body | `number` | yes | Payment term days number. |
| `PaymentTermType` | body | `number` | yes | Payment term type. |
| `DefaultTaxCode` | body | `string` | yes | Default tax code. |
| `Email` | body | `string` | yes | Primary supplier email. |
| `SupplierEmails[]` | body | `array<object>` | yes | Supplier email list. |
| `ReferenceNumber` | body | `string` | yes | Supplier reference number. |
| `SupplierName` | body | `string` | yes | Supplier display name. |
| `Void` | body | `boolean` | yes | Whether the supplier is void. |
| `IsActive` | body | `boolean` | yes | Whether the supplier is active. |
| `DefaultCostCode` | body | `string` | yes | Default cost code. |
| `DefaultCurrencyId` | body | `number` | yes | Default currency ID. |
| `TrustedStatus` | body | `boolean` | yes | Trusted supplier status. |
| `BankAccountNumber` | body | `string` | no | Supplier bank account number. |
| `BankSortCode` | body | `string` | no | Supplier bank sort code. |
