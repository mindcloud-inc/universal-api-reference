# Get Study FHIR JSON with ClinicalTrials.gov

## Endpoint

- **Method:** `GET`
- **Path:** `/studies/:nctId`
- **Base URL:** `https://clinicaltrials.gov/api/v2`
- **Official documentation:** [Get Study FHIR JSON](https://clinicaltrials.gov/data-api/fhir)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nctId` | path | `string` | yes | ClinicalTrials.gov study identifier. |
