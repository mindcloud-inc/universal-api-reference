# Update Tax Jurisdiction with Aspire

Updates an existing tax jurisdiction in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `TaxJurisdictions`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Tax Jurisdiction](https://cloud-api.youraspire.com/swagger/index.html#/TaxJurisdictions/TaxJurisdictions_Update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `TaxJurisdictionName` | body | `string` | yes |
| `FederalTaxPercent` | body | `number` | no |
| `Active` | body | `boolean` | yes |
| `TaxEntityJurisdictions[]` | body | `array<number>` | no |
| `TaxJurisdictionID` | body | `number` | yes |
