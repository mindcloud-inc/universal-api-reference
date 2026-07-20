# Update Supplier with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/supplier/update`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Update Supplier](https://api.quickfile.co.uk/d/v1_2/Supplier_Update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SupplierID` | body | `number` | yes | QuickFile SupplierID to update. |
| `CompanyName` | body | `string` | no | Updated supplier company or trading name. |
| `SupplierReference` | body | `string` | no | Updated external reference or short account code. |
| `Town` | body | `string` | no | Updated town or city. |
| `AddressLine1` | body | `string` | no | Updated first postal address line. |
| `Postcode` | body | `string` | no | Updated postal or ZIP code. |
| `CountryISO` | body | `string` | no | Updated two-letter ISO country code. |
