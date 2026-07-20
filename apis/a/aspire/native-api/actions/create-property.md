# Create Property with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `Properties`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Property](https://cloud-api.youraspire.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PropertyName` | body | `string` | yes | — |
| `PropertyNameAbr` | body | `string` | no | — |
| `PrimaryContactID` | body | `list<number>` | no | Choose an option from the list or map the Contact ID from a previous step. |
| `BranchID` | body | `list<number>` | yes | — |
| `TaxJurisdictionId` | body | `list<number>` | no | — |
| `PaymentTermsID` | body | `list<number>` | no | — |
| `PropertyStatusID` | body | `list<number>` | no | — |
| `AccountOwnerContactID` | body | `list<number>` | no | — |
| `AddressLine1` | body | `string` | no | — |
| `AddressLine2` | body | `string` | no | — |
| `City` | body | `string` | no | — |
| `StateProvinceCode` | body | `string` | no | Enter a US state, US territory, or Canadian province. Use the two-letter UPS code (e.g., "IL" for Illinois, "ON" for Ontario) or enter the full name and we'll convert it to the two-letter code based on the input. Reference this list for available options: https://www.ups.com/worldshiphelp/WSA/ENU/AppHelp/mergedProjects/CORE/Codes/State_Province_Codes.htm |
| `ZipCode` | body | `string` | no | — |
| `Active` | body | `boolean` | no | Format: `toggle`. |
| `PaperlessInvoices` | body | `boolean` | no | Format: `toggle`. |
| `EmailInvoiceFlag` | body | `boolean` | no | Format: `toggle`. |
| `LeadSourceID` | body | `number` | no | — |
| `IndustryID` | body | `number` | no | — |
| `BillingContactID` | body | `list<number>` | no | — |
| `PropertyTags` | body | `string` | no | — |
| `ProductionManagerContactID` | body | `list` | no | — |
| `CountyID` | body | `number` | no | Use this when Locality is enabled |
