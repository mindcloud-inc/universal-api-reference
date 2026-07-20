# Create Supplier with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/supplier/create`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Create Supplier](https://api.quickfile.co.uk/d/v1_2/Supplier_Create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CompanyName` | body | `string` | yes | Supplier company or trading name to create. |
| `SupplierReference` | body | `string` | no | Optional external reference or short account code for the supplier. |
| `Town` | body | `string` | no | Town or city for the supplier address. |
| `AddressLine1` | body | `string` | no | First postal address line. |
| `Postcode` | body | `string` | no | Postal or ZIP code. |
| `CountryISO` | body | `string` | no | Two-letter ISO country code. |
