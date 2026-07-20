# Get Risk Analysis Failure Mode with Grand Avenue Software

Retrieves a risk analysis failure mode from Grand Avenue Software by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/RiskAnalysisFailureModes/:id`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `$expand` | query | `list<string>` | no | Send multiple values as a string. |
| `id` | path | `string` | yes | — |
