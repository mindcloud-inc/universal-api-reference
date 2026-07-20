# List Companies with PredictLeads

Retrieves companies from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/discover/companies`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Companies](https://docs.predictleads.com/api_endpoints/companies_dataset/retrieve_companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | query | `string` | yes | The response will include only companies located in the given country name or state name/abbreviation. |
| `sizes` | query | `string` | yes | Company size filter. Official docs describe one or more valid sizes; runtime succeeded with a scalar query value such as `11-50`. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
