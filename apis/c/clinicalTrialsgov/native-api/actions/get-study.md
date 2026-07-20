# Get Study with ClinicalTrials.gov

## Endpoint

- **Method:** `GET`
- **Path:** `/studies/:nctId`
- **Base URL:** `https://clinicaltrials.gov/api/v2`
- **Official documentation:** [Get Study](https://clinicaltrials.gov/data-api/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Return only selected fields. |
| `nctId` | path | `string` | yes | ClinicalTrials.gov study identifier such as NCT06100835. |
| `markupFormat` | query | `string` | no | Preferred format for markup fields. Accepted values: `0`, `1`. |
| `format` | query | `string` | no | Response format. Accepted values: `0`, `1`. |
