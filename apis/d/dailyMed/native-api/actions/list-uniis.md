# List UNIIs with DailyMed

Retrieves UNIIs from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/uniis.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List UNIIs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/uniis_api.cfm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unii_code` | query | `string` | no | Unique Ingredient Identifier code. |
| `active_moiety` | query | `string` | no | Active moiety related to a UNII code. |
| `rxcui` | query | `string` | no | RxNorm Concept Unique Identifier code. |
| `drug_class_code` | query | `string` | no | Pharmacologic drug class code. |
| `drug_class_coding_system` | query | `string` | no | Coding system for the drug class code. |
