# Create Service Tax Override with Aspire

Creates a new service tax override in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `ServiceTaxOverrides`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Service Tax Override](https://cloud-api.youraspire.com/swagger/index.html#/ServiceTaxOverrides/ServiceTaxOverrides_Post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ServiceID` | body | `number` | no |
| `StateProvinceCode` | body | `string` | yes |
| `LaborTaxable` | body | `boolean` | no |
| `MaterialTaxable` | body | `boolean` | no |
| `EquipmentTaxable` | body | `boolean` | no |
| `SubTaxable` | body | `boolean` | no |
| `OtherTaxable` | body | `boolean` | no |
