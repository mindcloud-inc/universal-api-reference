# List Company Website Evolution with PredictLeads

Retrieves website evolution for a PredictLeads company.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_id_or_domain/website_evolution`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Company Website Evolution](https://docs.predictleads.com/api_endpoints/website_evolution_dataset/retrieve_company_s_website_evolution)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company ID or domain. |
| `first_seen_at_from` | query | `date` | no | Only return subpages first seen after the given date (ISO 8601). |
| `first_seen_at_until` | query | `date` | no | Only return subpages first seen before the given date (ISO 8601). |
| `page` | query | `number` | no | Page number of shown items. |
| `limit` | query | `number` | no | Limit the number of shown items per page. |
