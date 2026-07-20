# Create Tax Entity with Aspire

Creates a new tax entity in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `TaxEntities`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Tax Entity](https://cloud-api.youraspire.com/swagger/index.html#/TaxEntities/TaxEntities_Post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `TaxEntityName` | body | `string` | yes |
| `TaxPercent` | body | `number` | no |
| `Active` | body | `boolean` | yes |
