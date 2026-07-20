# Create Unit Type with Aspire

Creates a new unit type in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `UnitTypes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Unit Type](https://cloud-api.youraspire.com/swagger/index.html#/UnitTypes/UnitTypes_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UnitTypeName` | body | `string` | yes |
| `Active` | body | `boolean` | no |
