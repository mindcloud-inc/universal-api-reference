# Create Proposal with Better Proposals

Creates a proposal in Better Proposals.

## Endpoint

- **Method:** `POST`
- **Path:** `/proposal/create`
- **Base URL:** `https://api.betterproposals.io`
- **Official documentation:** [Create Proposal](https://betterproposals.io/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Company` | body | `string` | yes | Either a company ID or company name. When a name is provided, Better Proposals creates the company if needed. |
| `Cover` | body | `string` | no | Cover ID. |
| `Template` | body | `string` | no | Template ID. When provided, Better Proposals copies the template into the new proposal. |
| `DocumentType` | body | `string` | no | Document type ID or name. If omitted, Better Proposals uses the default proposal document type. |
| `Brand` | body | `string` | no | Brand ID. If omitted, Better Proposals uses the default brand. |
| `Currency` | body | `string` | no | Currency code in 3-letter format, for example USD. |
| `Tax` | body | `boolean` | no | Whether to apply tax. If omitted, Better Proposals uses the default brand setting. |
| `TaxLabel` | body | `string` | no | Tax label. If omitted, Better Proposals uses the default brand setting. |
| `TaxAmount` | body | `number` | no | Tax amount. If omitted, Better Proposals uses the default brand setting. |
| `Contacts[]` | body | `array<object>` | no | Array of contact objects with FirstName, Surname, Email, and Signature fields. |
| `MergeTags[]` | body | `array<object>` | no | Array of custom merge-tag objects with tag and value fields. |
