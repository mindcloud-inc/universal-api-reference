# List Company GitHub Repositories with PredictLeads

Retrieves GitHub repositories for a PredictLeads company.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_id_or_domain/github_repositories`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Company GitHub Repositories](https://docs.predictleads.com/api_endpoints/github_repositories_dataset/retrieve_company_s_github_repositories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company ID or domain. |
| `first_seen_at_from` | query | `date` | no | Only return GitHub repositories first seen after the given date (ISO 8601). |
| `first_seen_at_until` | query | `date` | no | Only return GitHub repositories first seen before the given date (ISO 8601). |
| `page` | query | `number` | no | Page number of shown items. |
| `limit` | query | `number` | no | Limit the number of shown items per page. |
