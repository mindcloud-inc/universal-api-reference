# List Similar Companies with PredictLeads

Retrieves similar companies from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_id_or_domain/similar_companies`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Similar Companies](https://docs.predictleads.com/api_endpoints/similar_companies_dataset/retrieve_company_s_similar_companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company's ID or domain. |
