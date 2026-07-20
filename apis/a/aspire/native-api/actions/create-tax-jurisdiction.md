# Create Tax Jurisdiction with Aspire

Creates a new tax jurisdiction in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `TaxJurisdictions`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Tax Jurisdiction](https://cloud-api.youraspire.com/swagger/index.html#/TaxJurisdictions/TaxJurisdictions_Post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `TaxJurisdictionName` | body | `string` | yes |
| `FederalTaxPercent` | body | `number` | no |
| `Active` | body | `boolean` | yes |
| `TaxEntityJurisdictions[]` | body | `array<number>` | no |
