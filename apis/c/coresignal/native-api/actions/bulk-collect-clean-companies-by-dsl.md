# Bulk Collect Clean Companies By DSL with Coresignal

Creates a bulk clean company DSL collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/company_clean/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Clean Companies By DSL](https://docs.coresignal.com/company-api/clean-company-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `es_dsl_query` | body | `object` | yes |
