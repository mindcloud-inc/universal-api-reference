# Update Tax Entity with Aspire

Updates an existing tax entity in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `TaxEntities`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Tax Entity](https://cloud-api.youraspire.com/swagger/index.html#/TaxEntities/TaxEntities_Update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `TaxEntityName` | body | `string` | yes |
| `TaxPercent` | body | `number` | no |
| `Active` | body | `boolean` | yes |
| `TaxEntityID` | body | `number` | yes |
