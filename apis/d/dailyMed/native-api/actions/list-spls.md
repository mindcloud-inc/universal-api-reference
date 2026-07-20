# List SPLs with DailyMed

Retrieves SPLs from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/spls.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List SPLs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_api.cfm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drug_name` | query | `string` | no | Generic or brand name to search for. |
| `ndc` | query | `string` | no | National Drug Code to search for. |
| `rxcui` | query | `string` | no | RxNorm Concept Unique Identifier. |
| `setid` | query | `string` | no | Set ID of a label. |
| `application_number` | query | `string` | no | New Drug Application number. |
| `published_date` | query | `date` | no | DailyMed published date in YYYY-MM-DD format. |
| `published_date_comparison` | query | `string` | no | Comparison for the published date: lt, lte, gt, gte, or eq. |
| `name_type` | query | `string` | no | Whether the drug name is generic, brand, or both. |
| `boxed_warning` | query | `boolean` | no | Whether the drug contains a boxed warning: true or false. |
| `dea_schedule_code` | query | `string` | no | DEA schedule code, such as none, C48672, C48675, C48676, C48677, or C48679. |
| `doctype` | query | `string` | no | FDA LOINC document/content type code for the label. |
| `drug_class_code` | query | `string` | no | Pharmacologic drug class code. |
| `drug_class_coding_system` | query | `string` | no | Coding system for the drug class code. |
| `labeler` | query | `string` | no | Name of the labeler for the drug. |
| `manufacturer` | query | `string` | no | Name of the manufacturer for the drug. |
| `marketing_category_code` | query | `string` | no | FDA marketing category code. |
| `unii_code` | query | `string` | no | Unique Ingredient Identifier code. |
