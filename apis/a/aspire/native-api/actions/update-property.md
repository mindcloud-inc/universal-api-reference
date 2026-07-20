# Update Property with Aspire

Updates a Property in Aspire

## Endpoint

- **Method:** `PUT`
- **Path:** `Properties`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Property](https://guide.youraspire.com/apidocs/properties-8)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PropertyID` | body | `list<number>` | yes |
| `PropertyName` | body | `string` | yes |
| `PrimaryContactID` | body | `list<number>` | no |
| `BillingContactID` | body | `list<number>` | no |
| `BranchID` | body | `list<number>` | yes |
| `AccountOwnerContactID` | body | `list<number>` | no |
| `TaxJurisdictionID` | body | `list<number>` | no |
| `PaymentTermsID` | body | `list<number>` | yes |
| `PropertyStatusID` | body | `list<number>` | yes |
| `StateProvinceCode` | body | `string` | no |
| `AddressLine1` | body | `string` | no |
| `AddressLine2` | body | `string` | no |
| `City` | body | `string` | no |
| `ZipCode` | body | `string` | no |
| `Active` | body | `boolean` | no |
| `ProductionNote` | body | `string` | no |
| `Note` | body | `string` | no |
| `PropertyNameAbr` | body | `string` | no |
| `CountyID` | body | `number` | no |
| `GEOPerimeter` | body | `number` | no |
| `SequenceNumber` | body | `string` | no |
| `Budget` | body | `number` | no |
| `SeparateInvoices` | body | `boolean` | no |
| `EmailInvoiceFlag` | body | `boolean` | no |
| `UpdateBranchReference` | body | `boolean` | no |
| `IndustryID` | body | `number` | no |
| `LeadSourceID` | body | `number` | no |
| `CompetitorID` | body | `number` | no |
| `PropertyGroupID` | body | `list<number>` | no |
| `Note` | body | `string` | no |
| `SnowNote` | body | `string` | no |
| `CollectionNotes` | body | `string` | no |
| `IntegrationID` | body | `number` | no |
| `PropertyTypeID` | body | `list<number>` | no |
| `ProductionManagerContactID` | body | `list<number>` | no |
