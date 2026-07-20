# Filter Compare And Export Responses with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/comparisionByQuestion`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Filter Compare And Export Responses](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | Comparison mode requested by Merren. |
| `surveyId` | body | `string` | yes | Survey identifier to filter and compare. |
| `filtersPayload` | body | `string` | no | Filter or comparison payload used by Merren reporting. |
