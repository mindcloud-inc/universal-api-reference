# List RxCUIs with DailyMed

Retrieves RxCUIs from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/rxcuis.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List RxCUIs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/rxcuis_api.cfm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rxcui` | query | `string` | no | Unique Identifier code for an RxConcept. |
| `rxstring` | query | `string` | no | RxString value of an RxConcept. |
| `rxtty` | query | `string` | no | RxNorm term type, such as PSN, SBD, SCD, BPCK, GPCK, or SY. |
