# List Drug Classes with DailyMed

Retrieves drug classes from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/drugclasses.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List Drug Classes](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/drugclasses_api.cfm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `class_name` | query | `string` | no | Name of the drug class. |
| `drug_class_code` | query | `string` | no | Pharmacologic drug class code. |
| `drug_class_coding_system` | query | `string` | no | Coding system for the drug class code. |
| `class_code_type` | query | `string` | no | Drug class type: all, epc, moa, pe, or ci. |
| `unii_code` | query | `string` | no | Unique Ingredient Identifier code. |
