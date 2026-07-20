# List Drug Names with DailyMed

Retrieves drug names from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/drugnames.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List Drug Names](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/drugnames_api.cfm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drug_name` | query | `string` | no | Generic or brand name of the drug. |
| `name_type` | query | `string` | no | Whether the drug name is generic, brand, or both. |
| `manufacturer` | query | `string` | no | Name of manufacturer for the drug. |
