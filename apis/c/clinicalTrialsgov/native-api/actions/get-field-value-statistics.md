# Get Field Value Statistics with ClinicalTrials.gov

## Endpoint

- **Method:** `GET`
- **Path:** `/stats/field/values`
- **Base URL:** `https://clinicaltrials.gov/api/v2`
- **Official documentation:** [Get Field Value Statistics](https://clinicaltrials.gov/data-api/about-api/study-data-structure)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | One or more data fields or pieces to analyze. |
| `types` | query | `string` | no | Optional field types to restrict the statistics. |
