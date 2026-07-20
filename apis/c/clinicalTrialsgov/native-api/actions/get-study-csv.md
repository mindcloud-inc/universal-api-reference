# Get Study CSV with ClinicalTrials.gov

## Endpoint

- **Method:** `GET`
- **Path:** `/studies/:nctId`
- **Base URL:** `https://clinicaltrials.gov/api/v2`
- **Official documentation:** [Get Study CSV](https://clinicaltrials.gov/data-api/about-api/csv-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nctId` | path | `string` | yes | ClinicalTrials.gov study identifier. |
