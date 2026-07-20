# Update Unit Type with Aspire

Updates an existing unit type in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `UnitTypes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Unit Type](https://cloud-api.youraspire.com/swagger/index.html#/UnitTypes/UnitTypes_Update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UnitTypeID` | body | `number` | yes |
| `UnitTypeName` | body | `string` | yes |
| `Active` | body | `boolean` | no |
