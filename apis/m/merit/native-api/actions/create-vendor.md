# Create Vendor with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendvendor`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Vendor](https://api.merit.ee/connecting-robots/reference-manual/vendors/create-vendor/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Vendor name. |
| `CountryCode` | body | `string` | yes | Two-letter ISO country code. |
| `VendorType` | body | `number` | yes | 1 for vendor, 3 for reporting entity. |
| `CurrencyCode` | body | `string` | no | Vendor currency code. |
| `VatAccountable` | body | `boolean` | no | Whether the vendor is VAT accountable. |
| `RegNo` | body | `string` | no | Vendor registration number. |
| `VatRegNo` | body | `string` | no | Vendor VAT registration number. |
| `PaymentDeadLine` | body | `number` | no | Default payment deadline in days. |
| `OverDueCharge` | body | `number` | no | Default overdue charge percentage. |
| `Address` | body | `string` | no | Vendor street address. |
| `City` | body | `string` | no | Vendor city. |
| `County` | body | `string` | no | Vendor county or region. |
| `PostalCode` | body | `string` | no | Vendor postal code. |
| `PhoneNo` | body | `string` | no | Primary phone number. |
| `Email` | body | `string` | no | Vendor email address. |
| `ReceiverName` | body | `string` | no | Receiver name. |
| `BankAccount` | body | `string` | no | Vendor bank account. |
