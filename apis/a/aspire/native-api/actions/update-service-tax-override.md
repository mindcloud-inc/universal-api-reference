# Update Service Tax Override with Aspire

Updates an existing service tax override in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `ServiceTaxOverrides`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Service Tax Override](https://cloud-api.youraspire.com/swagger/index.html#/ServiceTaxOverrides/ServiceTaxOverrides_Put)

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
| `ServiceTaxOverrideID` | body | `number` | yes |
