# List Commitment Contracts with Procore

Retrieves commitment contracts from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2.0/companies/:company_id/projects/:project_id/commitment_contracts`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Commitment Contracts](https://developers.procore.com/reference/rest/commitment-contracts#list-commitment-contracts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Unique identifier for the company. |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
