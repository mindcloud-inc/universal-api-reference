# Update Supplier with Zahara

Updates an existing supplier in Zahara.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/{businessUnitApiKey}/Supplier/Update/{{supplierId}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Update Supplier](https://ask.zaharasoftware.com/api-docs/update-supplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `supplierId` | path | `number` | yes | The Zahara supplier ID to update. |
| `Address` | body | `object` | yes | Supplier address object. |
| `BusinessUnitId` | body | `number` | yes | Business unit ID. |
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
| `ReferenceNumber` | body | `string` | yes | Supplier reference number. |
| `SupplierName` | body | `string` | yes | Supplier display name. |
| `Void` | body | `boolean` | yes | Whether the supplier is void. |
| `IsActive` | body | `boolean` | yes | Whether the supplier is active. |
| `DefaultCostCode` | body | `string` | yes | Default cost code. |
| `DefaultCurrencyId` | body | `number` | yes | Default currency ID. |
| `TrustedStatus` | body | `boolean` | yes | Trusted supplier status. |
| `BankAccountNumber` | body | `string` | no | Supplier bank account number. |
| `SupplierId` | body | `number` | yes | Supplier ID echoed in the update body. |
| `BankSortCode` | body | `string` | no | Supplier bank sort code. |
| `DefaultNominalCodeId` | body | `number` | yes | Default nominal code ID. |
| `DefaultTaxCodeId` | body | `number` | yes | Default tax code ID. |
| `DefaultCostCodeId` | body | `number` | yes | Default cost code ID. |
| `LastUpdated` | body | `string` | yes | Supplier last-updated timestamp. |
| `DateCreated` | body | `string` | yes | Supplier created timestamp. |
